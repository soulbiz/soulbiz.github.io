---
layout: post
title: "How To TagCloud"
categories: howtos
tags: [jekyll,guide,tagcloud,howto]
image:
  feature: tagcloud.jpg
  teaser: tagcloud.jpg
---

## Tag-Cloud

El nostre fragment de codi per generar la tag-cloud segueix els 
següents passos:

### 1. Iterem per tots els ``tags`` de ``site.tags``:

Aquí és on agafarem tots els tags dels Front-Matter dels posts.
	
### 2. Processem els tags dins d'elements ``<a>`` (enllaços):

Aquí és on aprofitem per generar la url corresponent per cada "tag".
	En aquest cas redirigim al propi "index" de tags que tindrem a la
	pròpia pàgina actual.

### 3. Dins l'enllaç, definim l'estil (tamany) de presentació corresponent.
	
Per fer-ho relatiu al número de posts amb aquest tag,
	en aquest cas multipliquem el número de posts per 30
	i sumem aquest número al percentatge base que establirem
	pel ``font-size``.	
	
D'aquesta forma obtindriem:
	
Un "tag" amb 4 posts:
		
		(4*30)+70 = **190%** de font-size.

### 4. Per acabar d'estilitzar, podem aplicar un estil CSS adient!

En aquest cas faig servir l'icona de "tag" de "fontawesome.io/"
	inclosa en el seu CSS, amb un estil afegit personalitzat.

