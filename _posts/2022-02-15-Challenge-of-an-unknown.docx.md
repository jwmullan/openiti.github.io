---
title: "The Challenge of an Unknown Typeface"
layout: post
excerpt: "When I came to the University of Maryland, I wanted to do a computational literary study of contemporary Persian novels. To do that, I started collecting PDFs of all the Persian novels that I could find, around 600 titles at present. I was particularly interested in finding digital copies of the works of my favorite writer, Houshang..."
image: /assets/images/main-images/Isfahan_Lotfollah_mosque_ceiling_symmetric_narrow_border.png
author: "Mehdy Sedaghat Payam"
---

When I came to the University of Maryland, I wanted to do a computational literary study of contemporary Persian novels. To do that, I started collecting PDFs of all the Persian novels that I could find, around 600 titles at present. I was particularly interested in finding digital copies of the works of my favorite writer, Houshang Golshiri, so I was overjoyed when I found his last novel *The Book of Genies* (1998).

Unfortunately, none of the OCR engines online worked well enough to convert these books (or any other book, for that matter) into text files of the kind that computers can read and perform computational analysis on. Luckily, that same year, Roshan Institute for Persian Studies at the University of Maryland had [won a grant from The Andrew W. Mellon Foundation](https://medium.com/@openiti/openiti-aocp-9802865a6586) to develop an OCR engine for Persian and Arabic texts, which I could use to extract text from the novels. However, the task of producing text files from the original PDFs I had gathered proved to be more difficult than I had anticipated.

In the summer of 2020, I joined the *OpenITI AOCP* project as a team leader for training data production. In this role I had to upload PDFs of books into an instance of eScriptorium hosted on the University of Maryland's Simorgh server. On that website, I had to segment the files and then use the OCR model trained by the technical team to transcribe them. After that I had to go through the results that eScriptorium had produced and correct them if they were not transcribed properly. The results were different for each book. Sometimes the engine had correctly transcribed almost all of the words and sometimes there were a few words in each line that needed to be corrected.

Since my own research interests lie in modern Persian literature, I also started experimenting with OCRing a few Persian novels. Initially, the results I got were horrendous. The first novel that I transcribed, as you might have guessed, was Golshiri's *The Book of Genies*. The first results for the book looked like this (Figure 1):

![](/assets/images/posts/Mehdy Sedaghat Payam (1)/media/image2.png)

![](/assets/images/posts/Mehdy Sedaghat Payam (1)/media/image5.png)

*Figure 1. Inaccurate OCR sample from Golshiri's* Book of Genies.

Such a poor result was something that I had not seen from any of the books that I had transcribed previously. However, this should not have been entirely surprising. *OpenITI AOCP* had been focused on improving OCR for premodern Islamicate studies. The books and typefaces that we had initially focused on and produced training data for in the early part of this project were printed in typefaces that were most commonly seen in older works. As the project progressed and as we produced more training data, the model began to yield better results on almost all typefaces.

But unfortunately, it still could not transcribe Golshiri's work well (Figure 2).

![](/assets/images/posts/Mehdy Sedaghat Payam (1)/media/image1.png)

![](/assets/images/posts/Mehdy Sedaghat Payam (1)/media/image3.png)

*Figure 2. Second attempt on Golshiri's* Book of Genies.

This was alarming to me because this model had worked quite well even on obscure typefaces. I brought this issue up with the wider *OpenITI AOCP* team in our biweekly technical meeting. Given the recent publication dates of the novels and the significant differences between the typefaces we had dealt with and the typeface I was trying to OCR, the technical team advised me that this typeface was likely [born digital](https://primarysources.yale.edu/what-does-born-digital-mean). Thus, we did not have it represented in our training data.

There was good news, though. All I needed to do was identify the typeface, after which the technical team could produce some artificial training data for it. Microsoft Word helped make this identification process easier, quickly informing me that this typeface was called [Tahoma](https://docs.microsoft.com/en-us/typography/font-list/tahoma). I contacted the technical team with this information, and a week later they sent me a new generalized transcription model based on all of our existing training data in addition to this new artificial training data. The results were amazing (Figure 3).

![](/assets/images/posts/Mehdy Sedaghat Payam (1)/media/image6.png)

![](/assets/images/posts/Mehdy Sedaghat Payam (1)/media/image4.png)

*Figure 3. Improved results in eScriptorium.*

Now this was a text that, despite its few minor errors, was good enough for computational analysis. Finally, I was able to convert the book to a usable plain text format.
