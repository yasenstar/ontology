 Using Protégé

# Documentation
(Protege Desktop)

Protege: https://protege.stanford.edu/support.php



Protege 5 Documentation:

https://protegeproject.github.io/protege/



Protege Desktop User Documentation:

https://protegewiki.stanford.edu/wiki/ProtegeDesktopUserDocs




## 1. Installation

### Download Page

### Installing Protege on Mac OS X

### Installing Protege on Windows

### Installing Protege on Linux

## 2. Getting Started

### Navigation

#### Switching among tabs

##### Entities Tab

##### OWLViz

###### Prerequisite: GraphViz

###### OWLViz documentation

#### Using "Search..." (ctrl+F)

### Reasoning

#### Protege comes with a built-in reasoner called HermiT

### Reconfigure the User Interface

### Human Readable Entity Names

### Pizzas in 10 Minutes
 (see:pizza.owl)
#### pizza.owl

## 3. Editor features

### Views

#### Annotations

#### Class Description

#### Class Hierarchy

#### Data Property Hierarchy

#### Imported Ontologies

#### Individual Description

#### Instances

#### Object Property Characteristics

#### Object Property Description

#### Object Property Hierarchy

#### Ontology Header

#### Ontology Metrics

#### Usage

### Menus

#### File > Export inferrred axioms as ontology

#### Edit > Find

#### File > Gather ontologies

#### File > Loaded ontology sources

#### File > New

#### File > Ontology libraries

#### File > Open

#### File > Open from URL

#### File > Open recent

#### File > Reload

#### Refactor > Rename entity

#### File > Save

#### File > Save As

#### Reasoner > Start Reasoner

#### Reasoner > Synchronize reasoner

### Protege preferences guide

### Naming and rendering of entities

### Protege Expression Editor

#### Class Expression Syntax

Class expressions are used to describe individuals that share common characteristics. This includes both class names (or named classes) and complex class expressions. The table below presents the keywords that are used to build up complex class expressions along with some examples. Class expressions can be nested to arbitrary depths in order to build up rich descriptions of the domain being modelled.



The Manchester OWL Syntax is used for presenting and writing various kinds of complex expressions in Protégé. This page provides a brief overview of the class expression syntax.

(https://www.w3.org/TR/owl2-manchester-syntax/)


##### some

###### hasPet some Dog
(Things that have a pet that is a Dog)

##### value

###### hasPet value Tibbs
(Things that have a pet that is Tibbs)

##### only

###### hasPet only Cat
(Things that have pets that are only Cats)

##### min

###### hasPet min 3 Cat
(Things that have at least three pets that are Cats)

##### max

###### hasPet max 5 Dog
(Things that have at most five pets that are Dogs)

##### exactly

###### hasPet exactly 2 GoldFish
(Things that have exactly 2 GoldFish as pets)

##### and

###### Person and (hasPet some Cat)
(People that have a pet that's a Cat)

##### or

###### (hasPet some Cat) or (hasPet some Dog)
(Things that have a pet that's a Cat or have a pet that's a Dog)

##### not

###### not (hasPet some Dog)
(Things that do not have a pet that's a dog)

#### Expression Editor Usage

### Manchester OWL Syntax

### DL Query Tab

### OWL Imports

### Axiom annotations

### Protege OWL Diff

## 4. Protege Advanced features

### The Bean Shell

### The Protege Server

## 5. Further setup / Configuration

### Adding more memory

### Double-clicking on OWL files (MacOS specified)

### Dealing with Protege preferences problems

#### Linux - stored in ~/.java/.userPrefs

#### Mac OS X - stored in ~/Library/Preferences/com.apple.java.util.prefs.plist

#### Windows - stored in the Windows Registry at HKEY_CURRENT_USER/Software/JavaSoft/Prefs

#### Java Preferences User Interface

You can also get the downloaded package from :my github folder


##### get jpui-0.4.0.jar

##### java -jar jpui-0.4.0.jar

### Working with firewalls and proxies

## 6. Protege plugins

### Auto Update plugins

### List of Protege Plugins

### CO-ODE Protege Plugins

#### Annotation template
 (see:pizza.owl)
#### Matrix
 (see:pizza.owl)
# WebProtege

## WebProtege Overview

## WebProtege User Guide

# Protege OWL Tutorial

## Tutorial in Protege Website

Not maintained in recent years


## Pizza OWL Tutorial by Michael DeBillis

## My Playlist of Pizza OWL practical videos (Referred by Michael)

## My Pizza OWL practice GitHub Repo

# Ontology Development 101

## Steps for making Ontology

### Step 1. Determine the domain and scope of the ontology

### Step 2. Consider reusing existing ontologies

#### List of Ontologies by W3C

##### The Dublin Core (DC) ontology

##### The Friend Of A Friend (FOAF() ontology

#### DAML Ontology Library

#### UNSPSC

#### Wine information

#### FIBO - The Financial Industry Business Ontology

#### SUMO - Suggested Upper Merged Ontology

#### NIST Common Core Ontologies

##### CCO in GitHub

#### Traditional Chinese Medicine (TCM) Domain Ontology

### Step 3. Enumerate important terms in the ontology

### Step 4. Define the classes and the class hierarchy

### Step 5. Define the properties of classes-slots

### Step 6. Define the facets of the slots

#### Slot cardinality

#### Slot-value type

#### Domain and range of a slot

The basic rules for determining a domain and a range of a slot are similar:

- When defining a domain or a range for a lot, find the most general classes or class that can be respectively the domain or the range for the slots.
- On the other hand, do not define a domain and range that is overly general: all the classes in the domain of a slot should be described by the slot and instances of all the classes in the range of a slot should be potential fillers for the slot.
- Do not choose an overly general class for range (i.e., one would not want to make the range THING) but one would want to choose a class that will cover all fillers.


##### Domain: The classes to which a slot is attached or a classes which property a slot describes, are called the domain of the slot

##### Range: Allowed classes for slots of type Instance are often called a range of a slot.

### Step 7. Create instances

## How many is too many and how few are too few?

### If a class has only one direct subclass there may be a modeling problem or the ontology is not complete.

### If there are more than a dozen subclasses for a given class then additional intermediate categories may be necessary

## When to introduce a new class (or not)?

### Subclasses of a class usually (1) have additional properties that the superclass does not have, or (2) restrictions different from those of the superclass, or (3) participate in different relationships than the superclasses

### Classes in terminological hierarchies do not have to introduce new properties

## A new class or a property value?

### If the concepts with different slot values become restrictions for different slots in other classes, then we should create a new class for the distinction. Otherwise, we represent the distinction in a slot value.

### if a distinction is important in the domain and we think of the objects with different values for the distinction as different kinds of objects, then we should create a new class for the distinction.

### A class to which an individual instance belongs should not change often.

## An instance or a class?

### Individual instances are the most specific concepts represented in a knowledge base.

### If concepts form a natural hierarchy, then we should represent them as classes

#### Only classes can be arranged in a hierarchy -- knowledge-representation systems do not have a notion of sub-instance.

## Limiting the scope

### The ontology should now contain all the possible information about the domain: you do not need to specialize (or generalize) more than you need for your application (at most one extra level each way)

### The ontology should not contain all the possible properties of and distinctions among classes in the hierarchy.
