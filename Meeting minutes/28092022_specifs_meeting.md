# Expression of needs

CESR historians need interactive software to create their own scenarios for extracting content items from ancient document images.

The scenarios created could be reused and adapted for different books.
They would allow only the desired content elements to be extracted, such as dropped capital letter, banners, large letters, titles, paragraphs, words, print or handwritten character.


# Analysis of the existing situation

## Situation

After the document image has been binarised by Agora, with the possibility to choose between different binarisation algorithms, the black pixels are processed by scenarios that aim to group those that touch each other in order to label content items.

A set or subset (defined in the scenario) of the content items with their labels is extracted into an *ALTO* file which gives their position in the original image.
There is one file per image.

### Scenarios

Among all the images in a document/collection, the expert selects a typical one on which to build and test specific scenarios to extract pixel clusters, split them, merge them and label them.

The user can save their scenarios and run them on other collections.

Scenarios can lead to the labelling of pixel clusters but also to various operations on them that are defined by the expert using rules.
They can be edited to be merged or split, and run iteratively.


### Rules

The rules used by the scenarios are either labelling rules or merger rules.

The labelling rules concern the position, size and neighbourhood of the content items, for example:
- if the content item has coordinates x < 121p, it is given the label of the margin *note*.
- if the content item is located in the top 25% of the image, it is given the label *title*.
- if the content item is larger than 50p, it is given the label of *dropped capital letter*.
- if the content item has a right neighboor, it is given the label of *dropped capital letter*.

The merger rules concern only the neighbourhood of the content items, for example:
- if the distance between two content items is less than 10p horizontally, they are merged.
- if two successive content items are [some item] and [some other item], they are merged.
- all content items in the top 121p are merged and are given the label of *title*.


## Use cases

The software is used for 2 typical scenarios:
- extract content items and store them in a file system using:
- - a hierarchical structure: "results" directory -> one directory per content type -> one subdirectory per image -> thumbnail images
- - an explicit naming convention: locate thumbnail from name, for example: 1.10.5.1.5 (page.parag.line.word.character), 1.1 (dropped capital letter 1 of page 1)


## To change

Binarisation is problematic because it is not efficient enough.

In the case of handwritten documents, one or more characters, words or even lines tend to touch each other and are treated as the same content items.
Therefore, the extraction of handwritten content items is impossible because too many of them touch each other.

The objective is to use deepl learning to better extract the content items.
In a first version, 



# Feasibility analysis

