# Диаграммы

## Диаграмма последовательности
```mermaid
sequenceDiagram
    actor User as Пользователь
    participant System as Система
    participant Model as LLM-модель

    User->>System: Отправить вопрос
    System->>System: Обернуть вопрос в промпт
    System->>Model: Передать промпт
    Model-->>System: Вернуть ответ
    System-->>User: Показать ответ
```
## Диаграмма классов
```mermaid
classDiagram

    class User {
        +int id
        +string name
        +string Orders
        +string Location
        +string additional_information
    }

    class QuestionText {
        +int id
        +string text
        +datetime datetime_stamp
        +string context
    }

    class AnswerToQuestionGood {
        +string answer
    }

    class AnswerToQuestionStore {
        +string answer
        +string LinksToThePloicyDocuments
    }

    class AnswerToRequestGoods {
        +string answer
        +string LinksToTheGoods
    }

    class AnswerToRequestBuy {
        +string answer
        +string LinkToPayPage
    }

    User  -->  QuestionText
    QuestionText --> AnswerToQuestionGood
    QuestionText --> AnswerToQuestionStore
    QuestionText --> AnswerToRequestGoods
    QuestionText --> AnswerToRequestBuy
```