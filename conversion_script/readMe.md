# Instructions for adding blogs

## Fork the website repository
If you have not already forked this repository, click the fork option at the top right. If you already have a fork, go to that fork in your own GitHub (e.g. github.com/mabarber92/openiti.github.io) and update the fork.

## Set up a GitHub secret for the upload
If you are forking the repository for the first time, you will need to set up a dedicated secret (this is what the actions script uses to permit changes to your fork.
1. Go to your GitHub account (top right of GitHub), open the side bar by clicking on your user icon and then click settings
2. Click on 'Developer settings' (right at the bottom of the page in the left navigation bar)
3. Click on 'Personal access tokens' and in the dropdown click 'Tokens (classic)'
4. Click 'Generate new token' and in the dropdown 'Generate new token (classic)'
5. You will be prompted to enter your password
6. Add a note to help you remember what the token is for (e.g. 'openiti blog upload')
7. If you do not want to have to do this regularly, reset the expiration date for the token under 'expiration'
8. Click 'Generate token' at the bottom
9. You will be returned to the list of tokens - there you will see a string in a green box - click the copy button next to that string and keep it in a safe place (this is your access token)
10. Navigate back to your fork and click on the settings tab
11. Go to the 'Secrets and variables' tab in the left navigation and click 'Actions' in the dropdown
12. Click 'New repository secret'
13. In the 'Name' field type : BLOG_UPLOAD
14. Paste your access token into the 'Secret' field
15. Click 'Add secret'
16. All done - the blog upload process should now work without issue. Remember that if you set your token to expire you will need to repeat this process when the secret expires.


## Create a yml file for the blog post
The yml file is what describes your post and it's content. *Without a yml file, your blog will not be uploaded to the website*. For each docx file containing a blog, there should be a corresponding yml file. If uploading multiple blog posts at once, download the sample yml (new_header.yml) file from the input folder and use this as a template to produce yml files for each blog, and upload all in one go.

The yml file looks like this:
```
title: 
layout: post
image: /assets/images/main-images/Isfahan_Lotfollah_mosque_ceiling_symmetric_narrow_border.png
author: 
docx: 
tags:
```

At an absolute minimum, you must fill out the title, author, and docx fields.

### What each field is used for
#### header
```
image: /assets/images/main-images/Isfahan_Lotfollah_mosque_ceiling_symmetric_narrow_border.png
```
This is a preset field and it sets the image that appears in the banner at the top of the page. If you change this, you will need to upload the corresponding image, set in 'overlay_image' to the images folder. It is recommended to put it in the 'covers' folder, if you do so.

#### title
```
title:
```
The title of the blog between quotation marks (remember when uploading your docx in the next step to remove the title of the blog post from the docx if it is present). For example:
```
title: 'Dispatches from al-Tabari part 1'
```
#### Author
```
author:
```
The author of the blog. This is written as plain text, as you would like it to appear on the website
```
author: 'Jonathan Parkes Allen'
```
#### layout
```
layout: post
```
This specifies the layout used by the website. **DO NOT CHANGE THIS**

#### tags
```
tags:
```
This field lists any tags you would like to associate with the blog. A list of existing tag codes are found below, but you can create new ones. For example:
```
tags:
 - text-reuse
 - book-history
 - author-practice
```
#### docx
```
docx:
```
Provide here the exact name of the docx file that is being uploaded into the input folder. **WARNING: If this name does not match the file name exactly, the upload will fail** For example:
```
docx: tabari_blog1.docx
```


## Add the word docx to the folder
Once you have created a yml file for each blog, you need to add the docx and yml files to the input folder. Navigate to the 'conversion_script' folder, and from there to the 'input' folder. Click the 'Add file' dropdown and click 'Upload files' button and drag and drop your docx files into the folder. For the conversion script to work, your files must be saved in 'docx' format. If you have already prepared your yml files, they can also be dropped into the input folder.

## Go to actions and run the workflow

## Check the test website and make corrections

## Submit a pull request to the main website


# Useful data for filling out a yml file


