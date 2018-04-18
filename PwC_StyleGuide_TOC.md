# PwC Technical Documentation Style Guide # 
*PwC Confidential*

*Version 1.0.0*

<!-- TOC depthFrom:2 depthTo:3 -->

- [<u>The writing mindset</u>](#uthe-writing-mindsetu)
    - [Topic-based writing](#topic-based-writing)
    - [Writing re-usable topics](#writing-re-usable-topics)
- [<u>Language and grammar</u>](#ulanguage-and-grammaru)
    - [Voice](#voice)
    - [Tense](#tense)
    - [Mood](#mood)
    - [Articles](#articles)
    - [Contractions](#contractions)
    - [Prepositions](#prepositions)
    - [Verbs](#verbs)
    - [Abbreviations](#abbreviations)
    - [Capitalization](#capitalization)
- [<u>Formatting, punctuation, and organization</u>](#uformatting-punctuation-and-organizationu)
    - [List or table](#list-or-table)
    - [Colons](#colons)
    - [Commas](#commas)
    - [UI elements and interaction](#ui-elements-and-interaction)
    - [Dates and times](#dates-and-times)
    - [Figures and images](#figures-and-images)
- [<u>Documentation versioning</u>](#udocumentation-versioningu)
- [<u>White papers</u>](#uwhite-papersu)
- [<u>Glossaries</u>](#uglossariesu)

<!-- /TOC -->


The purpose of this style guide is to support developers in writing content for PwC technical solutions. This style guide provides a set of writing guidelines to apply a clear and consistent writing style.

* Use correct grammar and punctuation.
* Use active voice and present tense.
* Write clear, simple sentences.
* Be consistent.
* Avoid jargon, slang, and the like.
* Use the simplest terminology.

## <u>The writing mindset</u> ##

There are some fundamental concepts you need to be familiar with to be able to produce material that can be used and translated.

* Topic-based writing and minimalism work
* Write with re-use in mind

### Topic-based writing ###

Topic-based writing is a way of arranging texts (topics) into small individual chunks of content that can be read and understood on their own – without the need to give the full context of a whole chapter. The aim is to make it possible for the user to understand the topic when searching online, within a PDF, and when reading it on its own in isolation. 

Topic-based writing also enables the re-use of texts between different products and outputs. Before writing a new topic, look for existing topics that you can reuse. Existing topics for all of the standard features should be reusable, unless there is a significant difference with a new product, that is, when a new platform or software version is introduced.

#### Three basic topic types ####

* Concepts
* Tasks
* References

**Concepts**

Concept topics explain ideas that the user must understand to complete a task. Concepts answer ″What is...″ questions. They introduce technologies and features on a general level and give a summary of the main possibilities and use cases. 

The first sentence in a concept topic should expand on the heading and give the user a clear indication of what information will follow. In other words, there should be a logical connection between the heading and the text that immediately follows.  

**Tasks**

Tasks answer ″How do I?” questions, and have a well-defined structure that describes how to accomplish a task or goal. A task is the same as an instruction and should consist of a heading, followed by a numbered list or a single bullet. 

**References**

Reference topics provide quick access to information that users need to complete tasks. Reference topics typically provide users with information about the following types of elements:
* Screen UI
* Commands
* Shortcuts
* Settings
* Icons

### Writing re-usable topics ###

Writing all new topics with re-use in mind. We ensure reuse by following certain basic principles that also maintain control of content, quality and style. To be able to produce re-usable topics, you have to have a deep knowledge and understanding of the product functionality and how it will evolve.
* Avoid using product names in texts. Use ‘your device’ or ‘the device’ or ‘most devices’ or similar. 

## <u>Language and grammar</u> ##

Follow the guidelines below to apply a clear and consistent writing style.

### Voice ###

In general, use active voice (in which the grammatical subject of the sentence is the person or thing performing the action) instead of passive voice (in which the grammatical subject of the sentence is the person or thing being acted upon).

* **Not recommended**: The service is queried, and an acknowledgement is sent.
* **Recommended**: Send a query to the service. The server sends an acknowledgment. 

### Tense ###

Use active voice as much as possible. Active voice focuses on the performer of the action and is often clearer, shorter, and more direct than passive voice.

* **Not recommended**: Up to 500 files can be stored in the database.
* **Recommended**: You can store up to 500 files in the database.

### Mood ###

Use the appropriate mood for the information type:
* Use the imperative mood for requests or instructions, such as in procedures.
    + **Example**: Select one or more check boxes.
* Use the indicative mood to specify information, such as facts and explanations.
    + **Example**: The solution provides a powerful way to store information.
* Do not use the subjunctive mood in technical documentation.
    + **Example**: If you were about to save the file ...

### Articles ###

Always apply the correct articles (definite and indefinite) in our documentation. Articles increase clarity and ease translation.

* **Incorrect**: Delete object from editor.
* **Correct**: Delete an object from the editor.

### Contractions ###

Do not use contractions in technical information.

Contractions can cause difficulty for translation and for users whose primary language is not English. For example, *it’s* can be interpreted as *it is* or *it has*. Contractions can also contribute to an overly informal tone.

* **Incorrect**: The database doesn’t back up the information automatically.
* **Correct**: The database does not back up the information automatically.

### Prepositions ###

Use prepositions effectively to clarify the relationship between elements in a sentence.

Follow the guidelines below for using prepositions:
* Include prepositions to increase the clarity.
    + **Ambiguous**: Upload the file using this feature.
    + **Clear**: Upload the file by using this feature.
* Omit unnecessary prepositions. For example, omit the prepositions in phrasal verbs when the verb alone provides the same meaning.
    + **Incorrect**: print out
    + **Correct**: print
* Avoid using too many prepositions in a sentence. Too many prepositions can clutter the text. 
    + **Not recommended**: The report is a list of the status of all of the event monitors for this process.
    + **Recommended**: The report lists the status of all event monitors for this process.
* Use a preposition at the end of a sentence to avoid a stilted construction.
    + **Not recommended**: Click the item for which you want to search.
    + **Recommended**: Click the item that you want to search for.
* Use a prepositional phrase instead of an apostrophe and the letter *s (’s)* to show the possessive form of abbreviations, brand names, product names, or inanimate objects.
    + **Incorrect**: The GUI’s layout is intuitive.
    + **Correct**: The layout of the GUI is intuitive.
    + **Incorrect**: Edit the object’s properties.
    + **Correct**: Edit the properties of the object.

### Verbs ###

Use clear and concise verbs with the appropriate mood, person, tense, and voice.

Follow the guidelines below for using verbs:
* Avoid using words that primarily function as verbs as nouns or adjectives.
    + **Incorrect**: the debug function
    + **Correct**: the debugging function
* Avoid using a phrasal verb (a verb and a preposition) if the verb alone provides the same meaning.
    + **Incorrect**: print out
    + **Correct**: print
* When you write a sentence that includes two coordinate clauses, do not omit the verb from the second clause.
    + **Incorrect**: The file names are displayed in uppercase characters and the other file attributes in lowercase characters.
    + **Correct**: The file names are displayed in uppercase characters, and the other file attributes are displayed in lowercase characters.

### Abbreviations ###

Abbreviations include initialisms, acronyms, and shortened words. 

Use abbreviations under the following conditions:
* Their meanings are clear.
* They make the information easier to understand.
* They are recognized more easily than their spelled-out forms, for example, HTML.
* Space is limited, for example, in a table or detailed diagram.

Follow the general guidelines below for abbreviations:
* Do not use an abbreviation as a noun unless the sentence makes sense when you substitute the spelled-out form of the term.
    + **Incorrect**: The tutorials are available as PDFs.
    + **Correct**: The tutorials are available as PDF files.
* Do not use abbreviations as verbs.
    + **Incorrect**: You can FTP the files to the server.
    + **Correct**: You can use the FTP command to send the files to the server.
* Do not use an apostrophe and the letter *s (’s)* to show the possessive form of an abbreviation. Make the abbreviation an adjective, or use the abbreviation in a prepositional phrase.
    + **Incorrect**: HTML’s properties are editable.
    + **Correct**: HTML properties are editable.

### Capitalization ###

Items such as headings, captions, labels, or interface elements generally follow one of two capitalization styles: sentence-style capitalization or headline-style capitalization.
* **Sentence-style capitalization**: This style is predominantly lowercase; capitalize only the initial letter of the first word in the text and other words that require capitalization, such as proper nouns. Examples of proper nouns include the names of specific people, places, companies, languages, protocols, and products.
    + **Example**: Requirements for Linux and UNIX operating systems
* **Headline-style capitalization**: This style uses initial uppercase letters for all significant words in the text. In headline-style capitalization, **do not** capitalize the initial letter of the following words:
    + Articles, except as the first word
    + Coordinating conjunctions
    + Prepositions, except as the first or last word
    + The to in an infinitive

## <u>Formatting, punctuation, and organization</u> ##

### List or table ###

Lists and tables are both ways to present a set of similarly structured items.

Consult the following table to decide which presentation to use:

|Item type    |Example                    |How to present           |
|:------------|:--------------------------|:-----------------------------------|
|Each item is a signgle unit. |A list of programming language names, or a list of steps to follow.|Use a numbered list, lettered list, or bulleted list.|
|Each item is a pair of pieces of related data. |A list of term/definition pairs.|Use a definition list, or a table in some contexts. |
|Each item is three or more pieces of related data. |A set of parameters, where each parameter has a name, a data type, and a description.|Use a table.|

Follow the general guidelines below to present the lists in the documentation:

|List type    |Used for                                         |
|:------------|:------------------------------------------------|
|Numbered list |Sequence of steps to be performed in order.|
|Lettered list |Options to choose among, especially mutually exclusive options.|
|Bulleted list |Set of items that is neither a sequence nor options.|
|Definition list |Set of terms, each with a description, definition, or explanation.|

### Colons ###

Use a colon to indicate that closely related information follows.

Follow the general guidelines to use colons in the documentation:
* Use a colon after an independent clause to introduce an inline list.
    + **Incorrect**: Remember to: encrypt the hard disk drive and set a password.
    + **Correct**: Remember to take these security measures: encrypt the hard disk drive and set a password.
* Use a colon after the label of a note.
    + **Example**: Important: Back up all data before you begin the migration.
* Do not insert a space before a colon, and insert one space after.
* Do not use a colon at the end of a heading or title.
* Use a colon after the introduction to a list, including a procedure or substeps of a procedure.    

### Commas ###

Use a comma to separate elements in a sentence, such as items in a series, clauses, or introductory phrases. If a sentence is complex or longer than 25 words, consider rewriting it, separating it into multiple sentences, or presenting its contents in a vertical list.
* Use a comma between independent clauses that are separated by a coordinating conjunction unless the clauses are short or closely related. Coordinating conjunctions are *and*, *but*, *or*, *nor*, *for*, *so*, and *yet*.
* Use commas to separate items in a series of three or more. Use a comma before the conjunction that precedes the final item.

### UI elements and interaction ###

When documenting a user interace, put UI element names in bold, and use appropriate nouns and verbs to describe how to interact with them. This applies to names for buttons, menus, dialogs, windows, list items, or any other feature in the UI that has a visible name.

### Dates and times ###

Spell out the names of months and days of the week in full. Give the full four-digit year, not a two-digit abbreviation.
* **Recommended**: January 10, 2018

### Figures and images ###

Use images only when they provide useful visual explanations of information that is otherwise difficult to express with words, or for screenshots of UIs that are important to the description.

## <u>Documentation versioning</u> ##

Documentation versioning is the process of assigning unique version numbers to unique states of the documentation. Within a given version number category, these numbers are generally assigned in increasing order and correspond to new developments in the documentation.

Use the three levels of numbering to identify the releases, such as *version x.x.x*. The first level digit denotes each release version, while the second and third level digit indicates the draft state of the release version, for example 1.1.1.

Always set the second and third level digit as zero to denote the official release version, for example 1.0.0, 2.0.0, 5.0.0, etc.

## <u>White papers</u> ##

A white paper is a detailed or authoritative report that states an organization's position or philosophy about a social, political, or other subject, or a not-too-detailed technical explanation of an architecture, framework, or product technology.

A white paper has the following components:
1. **Publication information**: The title, authors, publication date, and the copyright statement identify the publication.
2. **Table of contents**: If the paper has more than six subsections, include a table of contents with a list of all the headings, to make the topics easier to access in a PDF file. If the paper is viewed online, make sure that each heading in the table of contents links to its section.
3. **Introduction or abstract**: Briefly describe the topic, including the aspects that are discussed in the paper. In the first or second paragraph, describe your target audience.
4. **Body of the paper**: Use headings to help readers follow the content organization of the paper. Use only the number of heading levels that are needed to make your organization easy to understand.
5. **End matter**: You might want to include a conclusion and a question-and-answer section. Add appendixes, a list of references, a glossary, and links to related information as needed.
6. **Notices**: Include standard, required legal notices as defined by your company. 

Ensure that the appropriate people review the white paper to verify that it is accurate, complete, and legally appropriate. A typical approval process includes the following people:
* A technical contact or appropriate subject matter expert
* A product marketing representative
* Your manager
* A technical editor
* A company legal representative

## <u>Glossaries</u> ##

A glossary defines terms that are used in a product, set of products, or technology area. A glossary term can be a noun (including an abbreviation), a verb, an adjective, or an adverb.

Include the following types of terms in your glossary:
* Terms for concepts that are specific to your product or technology area.
* Industry-standard computing terms that have a special meaning in your product or technology area. For example, cursor has a meaning in relational database products that is different from the meaning of a cursor on a computer screen.

Arrange the glossary entries in alphabetic order.
