---
title       : Registration form
subtitle    : Collect user information 
author      : Roy Wang
job         : IT
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
--- bg:#ECF9F9

## Who would use this?

* This is a user informatin collection forum.
* This APP will collect user Registration Information and display it.
* The APP can be viewed at <a href =https://itexpertsh.shinyapps.io/Data_Products/ >shinyapp.io</a>

--- bg:#ECF9F9

## The ui.R file

* It uses the  Side and main layout.
* Text inpur filed will collect name, email.
* Radio buttons will collect the gendar .
* Date input will let the user to select the date birth .



```r
 dateInput("birth_date", label = h4("Date of Birth"), value = "1970-01-01")
```


--- bg:#ECF9F9

## The server.R file

* Will display all the input results.


```r
    output$name <- renderPrint({ input$name })
    output$email <- renderPrint({ input$email })
  
    output$gendar <- renderPrint({ input$gendar})
   
    
    output$birth_date <- renderPrint({ input$birth_date})
    
    output$odate<-renderPrint({input$date})
```


--- bg:#ECF9F9

## The Results

* The main panle will display the results


```r
             h4('Your Name')
             verbatimTextOutput("name")
             h4('Email')
             verbatimTextOutput("email"),
             h4('Gendar')
             verbatimTextOutput("gendar"),
             h4('Date of Birth')
             verbatimTextOutput("birth_date")
             h4('Registration Date')
             verbatimTextOutput("odate")
```


--- bg:#ECF9F9
