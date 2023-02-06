# Diagrams

Taio supports several ways to draw diagrams, all of which are implemented by inserting code that can be drawn as a diagram when previewing HTML.

Please refer to the their official documentation for more details, and here's a brief introduction on how to embed diagrams in Markdown.

## Sequence Diagrams

This feature is implemented using [js-sequence-diagrams](https://bramp.github.io/js-sequence-diagrams/), you can use it as following:

<pre style="padding-top: 12px; padding-bottom: 2px">
```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```
</pre>

```sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
```

That is, embedding the code using identifier `sequence`.

## Flowcharts

This feature is implemented using [flowchart.js](http://flowchart.js.org/), you can use it as following:

<pre style="padding-top: 12px; padding-bottom: 2px">
```flow
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

st->op->cond
cond(yes)->e
cond(no)->op
```
</pre>

```flow
st=>start: Start
op=>operation: Your Operation
cond=>condition: Yes or No?
e=>end

st->op->cond
cond(yes)->e
cond(no)->op
```

That is, embedding the code using identifier `flow`.

## Mermaid

This feature is implemented using [mermaid](https://mermaid-js.github.io/mermaid/#/), you can use it as following:

<pre style="padding-top: 12px; padding-bottom: 2px">
```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```
</pre>

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

That is, embedding the code using identifier `mermaid`.

## PlantUML [[zh]]([https://ngawangtrinley.github.io/docs.taio.app/#/cn/editor/diagrams?id=plantuml](https://ngawangtrinley.github.io/docs.taio.app/#/cn/editor/diagrams?id=plantuml-%e0%bd%96%e0%bd%bc%e0%bd%91%e0%bc%8d))

This feature is implemented using [PlantUML](https://plantuml.com/), you can use it as following:

<pre style="padding-top: 12px; padding-bottom: 2px">
```plantuml
Alice -> Bob: Authentication Request
Bob --> Alice: Authentication Response

Alice -> Bob: Another authentication Request
Alice <-- Bob: Another authentication Response
```
</pre>

<img src="http://www.plantuml.com/plantuml/svg/SoWkIImgAStDuNBCoKnELT2rKt3AJx9IS2mjoKZDAybCJYp9pCzJ24ejB4qjBk42oYde0jM05MDHLLoGdrUSoeLkM5u-K5sHGY9MGw6ARNHryQb66EwGcfS2T300">

That is, embedding the code using identifier `plantuml`.

> Alternatively, you can also use @startuml and @enduml to wrap the code blocks.
