# Imperiia Project, Undoing Empire : metadata interview transcript

## Project name

History of Plants in Odessa. 

## Authors

Data model designed by Kelly O'Neill  
Davit Gasparyan, Olga Kiyan, Jackie Erlon-Baurjan (data contributors)

## Point of contact 

Kelly O’Neill 
email: [imperiia@fas.harvard.edu] (mailto:imperiia@fas.harvard.edu)

## Project data access

Available via Harvard Dataverse > The Imperiia Porject Data Drive:
[https://doi.org/10.7910/DVN/GNPAYF/](https://doi.org/10.7910/DVN/GNPAYF)
 

## File names

* Attributes only: flora\_odessa.csv  
* Shapes  
  * Points: flora\_odessa\_settlements.geoJSON  
  * Lines: flora\_odessa\_rivers.geoJSON  
  * Polygons: flora\_odessa\_habitat\_areas.geoJSON  
* Bounding boxes: flora\_odessa\_observation\_areas.geoJSON


## Time period the data represents

The source was published in 1892. The observations were all made between 1890 and 1891\. 

## Geographic coverage

Odessa province or Oblast   
Black Sea   
Ukraine  
Russian Empire 

## Thematic keywords

Botany   
History of Science  
Empire  
Imperial History  
Russian Empire  
Biodiversity  
Plants

## Abstract

This is a historical dataset describing the scientific observation of plant species in the region around Odessa in the late 19th century. Our intentions were to enhance and make an original contribution to knowledge of the history of biodiversity in the former Russian Empire and modern Ukraine. The project also aimed to provide a model for describing plant habitats and other non settlements, other geographical features that are not simply settlements or rivers. The project is also intended to provide a model for creating GIS data out of historical sources. We aim to make the original the primary source material more usable by ascribing a set of thematic keywords and developing the data as a relational data model, in order to make querying and filtering easier. 

## Sources

### Materialy dl︠i︡a flory ︠i︡ugo-zapadnoĭ chasti Odesskago uieda, Khersonsʹkoï guberniï = Material for a flora of the southwestern part of Odessa district
Shesterikov, P. S. (Petr Stepanovich) / Odessa : Typ. A. Shud'khe  
1894  
[https://id.lib.harvard.edu/alma/990063817950203941/catalog](https://id.lib.harvard.edu/alma/990063817950203941/catalog)

This is a work by Petr Stepanovich, who was half botanist, half librarian. He’s much more famous for being a librarian. It was published in the Russian language. It draws on lots of previous flora that were published by some of his contemporaries and his predecessors. 

We did also rely on geonames and openstreetmap for modern location triangulating. 

We have a couple of historical maps as well that we have been using for, for the spatial data as well. 

### Plan goroda Odessy   
sostav. gorodsk. zemlemi︠e︡r M.M. Diterikhs
[Odessa?] : [Gorodskoĭ zemlemi︠e︡r], 1894.
[https://lccn.loc.gov/2014592004](https://lccn.loc.gov/2014592004)

One is a town plan of Odessa from 1894. It’s contemporary with the primary source. We've used that for locating a lot of the neighborhoods and little plantations around the city of Odessa. 

### [Topograficheskie karty evropeĭskoĭ chasti Rossiĭskoĭ Imperii masstaba 1:126 000] = [Topographic maps of the European part of the Russian Empire at scale 1:126,000]
Russia. Armii︠a︡. Glavnyĭ shtab. Kartograficheskoe zavedenīe
[Saint Petersburg?] : [General Staff of the Russian Army], [1865?-1917?]
[https://lccn.loc.gov/2017588176](https://lccn.loc.gov/2017588176)

And then there are a couple of sheets from the military topographical survey of the Russian of European Russia that was conducted in the 1860s and published in the 1870s and 1880s. There are a couple of those sheets that also describe the region around Odessa and we've used those as well for locating things like where the sandy areas were and where the ravines were and things like that. 

### Global Biodiversity Index. 
Whenever we found a plant, whenever there was a plant species, we included the unique identifier from the global biodiversity index. So someone could go there, that is the authoritative place.   
[https://gbif.org/](https://gbif.org/)

## Larger body of work

The Imperial project, the scalar project.   
[https://scalar.fas.harvard.edu/imperiia/](https://scalar.fas.harvard.edu/imperiia/)

## Process steps and methods

The first step was to familiarize ourselves with the way that plant observations are structured in the primary source and to identify the various attributes of each plant that could be isolated and recorded in the data set. We decided to use a web based platform called NodeGoat to record all of our data. Our data creation was not a linear process at all. We iterated on the data model throughout the course of the project. We cross referenced every plant in the global Biodiversity Information facility, the GBIF, to see if it’s identified there and that helped us make sure that we were recording the plant name correctly. We did maintain the spelling originally given in the source rather than editing it, but we would record any discrepancies. And the biggest source of discrepancy was definitely with the plant family that the species was being allocated to because botanists have changed their mind over time about how plant families work. 

The source is certainly not tabular data, it’s more like a diary. The author would give the name, it always starts with the Latin name of the plant species. And then he would give some description of where it can be found, the kinds of habitats that he found it in. And if he didn't find it at all himself, he would always point that out, that he was not able to make a direct observation in cases where previous or other botanists had made observations of that plant. He would record what they had said and then add his appraisal of whether or not the other botanists knew what they were talking about. So there's a constant little commentary going on. 

He gives the date for most of his observations. That's the one piece of information that we did not record consistently. We did not record it consistently because it was not really in keeping with our focus, which was more on trying to figure out how to map the places where these plants were found. It was not a high priority, and a little bit cumbersome to record. 

The source is also 19th century style Russian, so we’re translating as well. Methods-wise, there was a lot of back and forth with the graduate students, I had to sometimes just correct if they didn't happen to know this archaic term that was used to describe something differently than what they think it's used for, so in terms of motivations, in addition to creating this resource, this was also an educational opportunity for the data creators to learn historical Russian. Most of the graduate students who work for me don't work on the historical period. Most come to Harvard for the master's program, which has a contemporary focus. Many students have experience in history, but it might only go back to the Soviet period. So it's rare to have students who are at all familiar with 18th and 19th century sources. 

In terms of spatial data, I know we have a lot of files. Most of the places on this list fall into one of three buckets:

1. A historical place that can be correlated with a place that currently exists in the world. For example, there's the town of Odessa, which goes back to the early the late 18th century, and it happens to also exist right now. So, if you want to find Odessa, you can go search for it in GeoNames and get the centroid of the contemporary town space. You can also find it in lots of historical sources.

2. Historical places that for one reason or another are no longer known to modern gazetteers. GeoNames doesn't know about it, OpenStreetMap doesn't know about it. Nobody knows about it. It just isn't part of the modern world. That's a smaller bucket. A lot of those places are things like “Wagner Farm”. Of course, it's not going to occur in GeoNames, but it is a named place. For these observations we relied on historical sources like maps, and created bounding boxes for the areas.

3. There are many entries in the flora that say things like, “This plant grows in sandy areas near the Black Sea.” It's not a place, but it's some sort of location, so we needed to figure out a different way to handle creating geographic data for these kinds of observations. Bucket three are represented by polygons, but they’re not named places, so for instance, they represent something like “coastal areas”, or “sandy areas”, “marshes,” so essentially habitat areas.

### Spatial files

Rivers  
Points are known, settled locations – Centroids for places that have a population of a certain number  
Polygons \- Habitat areas  
Bounding boxes \- Geographically identified but not modern places

## Challenges

The biggest challenge and it's a conscious challenge, not a surprise, is trying to figure out how to map places that are impossible to find. But the thing is that you can get pretty close. We have a reasonable amount of knowledge of where these habitat areas are based on a layering of really great contemporary data that shows us right now, which is at least a starting point. OpenStreetMap data can show us different vegetation types, and other land use. So we have that as an approximation. Then we have the military topographic survey maps. So, to a certain extent we can recreate these various historic land use areas. We will never be able to map the actual location of the plant that Chekov, saw because he doesn't tell us exactly where it was, but we can approximate the typical land use classes you’d expect to see. So of course there's ambiguity and inaccuracy embedded in the data, and as you're working in a GIS environment, I think people's alarm bells go off, “Oh but it's not accurate, so I can't use it.” So I think that's the biggest challenge is to say, no, you can act, you can come to a place, you can learn so much from this data. Despite the fact that the accuracy isn't ideal. 

## Pride points

There's an observation type field and that tells you whether each observation in the list was a direct observation, Bychkov himself or an indirect observation that he's reporting on. And that's really important because that is firs thand versus second hand knowledge. So when you're mapping this data, you can see here are all the plants that he saw himself. And, and then here are the places where supposedly those plants existed. But sometimes he's quite doubtful that those plants existed at all. 

The other value is the habitat field. There are a relatively small number of named places in this data set. Most of the plants that were observed were observed in the immediate vicinity of Odessa in maybe a dozen little villages surrounding the main town. That's where he worked. That was the place that he just paced back and forth, his work area. So it's not like there are a million different villages named in this data set. But within that space, he notes the distinction between every little micro in a region in the ecosystem. So we recorded each of the habitat identifiers or descriptors that he used for each plant. We had to go through those and assemble them, and narrow them down to reduce redundancy in that list. So there are some places that only occur in salt marshes and there are some that occur in salt marshes and meadows, damp meadows. And so this very, very long list of 820 different species – we carved the habitats down to a much more manageable set. So that is very valuable because essentially what we compiled was like here are all the viable feature classes for this region. 

## Data integrity

Whenever there's a piece of information that's simply not given in the primary source, we recorded that as not specified. So in theory there are no blanks in the data. If there is a blank or null value, it is a mistake. There are definitely a lot of times that the entries are not 100% consistent. There are lots of times where he doesn't tell you whether it's a weed or a wildflower, you know, he'll just skip that part. So we recorded that. We made no assumptions in our recording of the data, we recorded it in the way that Skov presents it. So even if we think he was wrong, for example, if the family name of a species is given an, and it's technically incorrect, we recorded his and we have a note that explains the discrepancy with modern stuff. 

Other data integrity topics might be language issues. We recorded place names and personal names um as they were given in the source, and a lot of the botanists who he references are Germans or French, etc. So sometimes their names are misspelled and sometimes the Latin names of some of the species are misspelled. So there are linguistic issues. And we were consistent in the way that we recorded anything that was a decision on our part in the documentation log. So anything you see in the data exists that way in the primary source or if there's a reason we’ve explained why it’s represented that way in the log. 

## Codebooks and Taxonomies

In the interview we noted that any notes related to these were forthcoming.

## Completion and maintenance

I would consider this data to be complete. I'm hoping that there will be a supplementary data set that will go through this process with a couple of other floras. And that will make the data a lot more powerful, but it would be the same method. I would not anticipate any need to change what we're publishing in this first edition. There is a possibility that if we add additional flora, the accompanying spatial data would become more accurate and it would supersede this first edition. 

## Access Use or Constraints

The only constraint that I would like to put on it would be a non-commercial kind of use. So, any kind of academic fair use educational stuff is absolutely great. 

For educational non-commercial use only. This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License, CC BY-NC-SA 4.0 DEED [https://creativecommons.org/licenses/by-nc-sa/4.0/](https://creativecommons.org/licenses/by-nc-sa/4.0/)