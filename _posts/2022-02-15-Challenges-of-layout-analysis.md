---
title: "Challenges of Layout Analysis across Arabic-Script Training Data"
layout: post
excerpt: "Layout Analysis is the process of identifying regions (e.g., title, body text, footnotes, etc.) on a page of text before sending it through the OCR engine. Preparing documents to train our OCR models involves several distinct steps, including semantic annotation, fixing segmentation errors, and editing faulty transcriptions. eScriptorium allows users to associate specific labels with regions..."
image: /assets/images/main-images/Isfahan_Lotfollah_mosque_ceiling_symmetric_narrow_border.png
author: "Şaban Ağalar"
---

Layout Analysis is the process of identifying regions (e.g., title, body text, footnotes, etc.) on a page of text before sending it through the OCR engine. Preparing documents to train our OCR models involves several distinct steps, including semantic annotation, fixing segmentation errors, and editing faulty transcriptions. eScriptorium allows users to associate specific labels with regions which follow [user-defined ontologies](https://lectaurep.hypotheses.org/documentation/escriptorium-tutorial-en). Having regions annotated in a document allows you to select certain region types to export (Figure 1). For example, you may export in a plain text format that has only the body of text, excluding page numbers, footnotes, titles, etc. This is why proper layout analysis is of primary importance for users who want to manipulate their OCR output.

![](/assets/images/posts/Şaban Ağalar (1)/media/image4.png)

*Figure 1. An export pane in eScriptorium*

The default configuration includes four tags--'commentary,' 'illustration,' 'main,' and 'title'--but it is possible to delete any one of them or add new ones. In labeling regions for layout analysis, we follow certain standards. We have not only added new regions but have also reconsidered the existing categories. Instead of the broader category of 'commentary,' we use 'marginal material' and 'footnotes' so that the critical apparatus appearing below a line at the foot of the page is separated from anything appearing in the left, right, or top margins. This is based on the assumption that what we label as footnotes are semantically distinct from the rest of the material that appears outside of the body of the text in most cases. Similarly, we replace the tag 'title' with two tags--'running title' and 'head'--to differentiate headers that appear outside of the body of the text from similar material appearing within it. We also label page numbers and catchwords in older printed books as separate regions.

![](/assets/images/posts/Şaban Ağalar (1)/media/image2.png)

*Figure 2. A document that is manually annotated. Different colors indicate different semantic regions (Birgivi. 2002. al-Ṭarīqa al-Muḥammadīya, Damascus: Dār al-Qalam)*

In practice, however, applying our standard semantic categories to all sorts of printed material produced in the Islamicate world proved to be less than easy. The diversity of unstandardized layouts in Arabic-script print materials often challenged the criteria we had agreed upon.

To begin with, it is not always easy to distinguish the body of a text from its surroundings. As an example, titles in between text blocks challenge readers to specify what is inside and what is outside of the text body. In such cases, our categorization of the headers as 'running title' and 'head' became useless (Figure 3).

Should *basmalas* located at the beginning of a page be treated as part of the body of a text? In form, they look like titles, but in terms of semantics, they are certainly not.

![](/assets/images/posts/Şaban Ağalar (1)/media/image3.png)

*Figure 3: A page that contains titles between text blocks (Saʻdī. 1832. Gulistān, Calcutta)*

For books printed in Arabic script, the distinction between illustration and text is not always self-evident. For example, *basmalas* or titles written in calligraphy tend to challenge our semantic categories (Figure 4).

![](/assets/images/posts/Şaban Ağalar (1)/media/image6.png)![](/assets/images/posts/Şaban Ağalar (1)/media/image5.png)

*Figure 4: Stylistic basmalas. (Birgivi. 2002. al-Ṭarīqa al-Muḥammadīya, Damascus: Dār al-Qalam; ʻAsalī, Bassām. 1988. Fann al-ḥarb al-Islāmī, Lubnān: Dār al-Fikr.)*

Even 'page number,' seemingly the most self-evident category of semantic regions, is challenged by uncommon layouts. As seen in Figure 5, we came across early printed Persian texts that contain two separate numbers, one at the top and one at the foot of the page. While the number at the top refers to the page number, the other one indicates the order of sections on that page. For lack of a better category, we label the section numbers as marginal material, but this hardly represents what the semantics of the region imply.

![](/assets/images/posts/Şaban Ağalar (1)/media/image1.png)

*Figure 5: Ḥāfiẓ. 1281 \[1864\]. Dīvān. Būlāq*

In conclusion, Arabic-script printed texts are full of surprises in terms of page layouts that cannot be easily standardized for regional annotations across different periods and languages. The majority of challenges that I have mentioned come from early printed material in the Islamicate world. By the twentieth century, we have more standardized book structures across both Arabic and Persian texts that are largely modeled on the modern layouts of printed materials in Western languages.
