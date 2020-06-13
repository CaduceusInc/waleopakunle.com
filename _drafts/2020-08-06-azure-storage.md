---
toc: true
comments: true
author: Wale
image: https://media.giphy.com/media/lrQ2T4iMddQhG/giphy.gif
categories: [Data-Engineer-Notes, Storage]
permalink: /news/:year/:month/:day/:title
---

```b4post.TODO
! 1change all references to "person" to Product catalog format

```

# Notes Source: [Storage in Azure - 1](https://docs.microsoft.com/en-us/learn/paths/store-data-in-azure/)

## Data Classification

Application data can be classified in one of three ways:

1. Sructured
1. Semi-structured
1. Unstructured

It's imporetant to learn how to classify your data so that you can choose the appropriate storage solution.

---

- Structured (or relational) data

---

Structured data is often stored in database tables with rows and columns with key columns to indicate how one row in a table relates to data in another row of another table.

Features:

  - Adheres to strict shared schema
  
  - Can be easily searched with query languages such as SQL (Structured Query Language).

  - Often stored in database tables with rows and columns with key columns to indicate how one row in a table relates to data in another row of another table.

{% include info.html text="*Downside of Structured Data*: forcing a consistent structure also means evolution of the data is more difficult as each record has to be updated to conform to the new structure." %}

---

- Semi-structured data

---

Semi-structured data is also referred to as non-relational or NoSQL data. This kind of data  is not stored in a relational format, as the fields do not neatly fit into tables, rows, and columns.

The expression and structure of the data in this style is defined by a serialization language.

Common formats:

- *xml (extensible markup language)*:
  
  - text based, so readabble by man and machine.

  - parsers are readily available.

  - has standards for schema, transformation, and even displaying on the web.

  *Example*:

  ```shell

  <Person Age="23">
    <FirstName>John</FirstName>
    <LastName>Smith</LastName>
    <Occupations>
        <Occupation Type="Health Worker">DOctor</Occupation>
        <Occupation Type="Data Scientist">Machine Learning Engineer</Occupation>
        <Occupation Type="Law & Order">Lawyer</Occupation>
   </Occupations>
  </Person>
  
  ```

  Properties of xml:

  - XML expresses the shape of the data using tags.

  - XML is flexible and can express complex data easily.

  {% include info.html text="*Downside of XML*:

  XML tends to be more verbose making it larger to store, process, or pass over a network. As a result, other formats have become more popular." %}

---

- JavaScript Object Notation (*JSON*)

  - Properties of json:

    - Has a lightweight specification

    - Relies on curly braces to indicate data structure.
  
    - Compared to XML, it is less verbose and easier to read by humans.

    - JSON is frequently used by web services to return data.

*Example* 

```person.json
{
    "firstName": "John",
    "lastName": "Doe",
    "age": "23",
    "hobbies": [
        { "type": "Sports", "value": "Golf" },
        { "type": "Leisure", "value": "Reading" },
        { "type": "Leisure", "value": "Guitar" }
    ]
}

``` 

It's closer to a key/value pair model than a formal data expression.

 {% include info.html text="*Downside of json*:
 json tends to be more programmer-oriented making it harder for non-technical people to read and modify." %}

---

- YAML Ain’t Markup Language (YAML)

   Features:

  - Data structure is defined by line separation and indentation

  - Reduces the dependency on structural characters like parentheses, commas and brackets.

  - More readable than JSON

  - Often used for configuration files that need to be written by people but parsed by programs


     ```person_attributes.yaml-sample
     firstName: John
     lastName: Doe
     age: 23
     hobbies:
      - type: Sports
        value: Golf
      - type: Leisure
        value: Reading
      - type: Leisure
        value: Guitar
     ```

     {% include note.html text="Read more about YAML here:

     [https://yaml.org/](https://yaml.org/), or check out the official python bindings [here](https://pyyaml.org/wiki/PyYAMLDocumentation)." %}

---

Unstructured Data

---

The organization of unstructured data is ambiguous. Unstructured data is often delivered in files, such as photos or videos. The video file itself may have an overall structure and come with semi-structured metadata, but the data that comprises the video itself is unstructured.

Examples of unstructured data include:

Media files, such as photos, videos, and audio files
Office files, such as Word documents
Text files
Log files

---
---
---
---

## [Determine operational needs](https://docs.microsoft.com/en-us/learn/modules/choose-storage-approach-in-azure/3-operations-and-latency)

When deciding what storage solution to use, think about how your data will be used. How often will your data be accessed? Is your data read-only? Does query time matter? The answers to these questions will help you decide on the best storage solution for your data.

```.TODO2
## Fix this...
This incomplete section.

%% Idea1 :::: Embed google form in blog pposts such as this to collect people's answers to the quiz questions.

%% Idea2:::: Show twitter feed from my list on my site?

%% Idea3::: Implement conversational bot on blog. Have it talk about societal concerns.

```