# WEEKLY SPECIFICATION REPORT

## DESCRIPTION

**Topic:** Drafting of specifications in regards to the brief with M. Ragot

**Objective:** Drafting the clarifications from M. Ragot on the right content to write

**Author:** Théo Boisseau

**Creation date:** 19.10.2022

**Time spent:** 4h

**Version:** 1.1

## SUMMARY

1. [METHODOLOGICAL BASES](#I.)
2. [CONSTRAINTS IN ANALYSIS AND DESIGN](#II.)
3. [SYNTHESIS OF ANALYSIS](#III.)


# I. METHODOLOGICAL BASES <a id="I."></a>

I should define experimental protocols and the project management method.

The experimental protocols will cover the teaching of the model, its testing, implementation, tools and conventions to be followed.

The project management method will define the milestones of the project, how often I will meet with the supervisor and deliver products.
In this case, it will highlight:
- an explanatory phase: designed as a practical study of the appropriate frameworks for each project functionality and punctuated by regular scientific discussions with the supervisor
- a development phase: organised by project functionality priority, and punctuated by regular meetings with the supervisor/client. In other words, just like an Agile method.


# II. CONSTRAINTS IN ANALYSIS AND DESIGN <a id="II."></a>

## EXTRACTOR(S)

Making a general extractor, which would extract the layout of all the EOCs on the page, may not be the most useful choice.

First of all, the user needs a modular solution that allows them to build the right scenario.

Secondly, the more things the model can extract, the more difficult it is to generalise.
Indeed, since the user needs as many potential characters as possible, even if it is not certain that these are the actual characters, they will play a much more important role in the objective function.
In this case, it might be harder to predict dropped capital letters or any other decoration.

As they are 3 main types of EOCs:
- decoration
- text
- additional text (annotations)

Making a model for each of them would allow much more modulability and less complexity.
Therefore, this seems to be the most appropriate choice.


## FRAMEWORKS <a id="II.FRAMEWORKS"></a>

Frameworks designed for Ancient Document Layout Analysis usually use additional features than others, in order to take into account broken characters, stains, poor paper quality, and so on.

The study of the different Frameworks should take into account the previous section, so that some may be better than others for certain tasks.


## LEARNING

It will be interesting to define hypothesis and risks in regard to the user needs.
Such as the future of their research or their potential other needs.
It will influence the product and the data sets.

The most important non-functionnal specifications about the learning will be the performance metrics, the performance expectations and the learning time.
With regard to datasets, the ways in which their completeness is promoted and how they should be labelled are essential.


# III. SYNTHESIS OF ANALYSIS <a id="III."></a>

I should present explicit **UML diagrams** in order to define and validate:
- Use cases
- Architecture and theoretical components

I should explain that studying the existing software in detail is not very relevant as it is a complete overhaul.
However, it will be useful to explain what it is and what functionality it provides.

