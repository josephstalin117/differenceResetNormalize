# 关于normalize.css和reset.css之间的区别  


## Indrotuction

**本文只列出reset之间的区别～**  
**顺序按normalize.css从上到下～**  
**本文约定R代表52framework，N代表normalize**
**reset中未涉及伪类**


1. [HTML5 display definitions](#HDD)  
2. [Base](#B)  
3. [Links](#L)
4. [Typography](#T)  
* [Embedded](#E)
* [Figures](#F)
* [Forms](#Fo) 
* [Tables](#Ta)


<h2 id="HDD">HTML5 display definitions</h2>  

* **main**  
属性R未指定  

* **cavas**  

N:    

    audio,
    canvas,
    video {
        display: inline-block;
    }

R：  
    
    canvas{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    canvas { 
      display:block;
    }
    
* **audio, video**  

N:

    audio,
    canvas,
    video {
        display: inline-block;
    }  
 
R:

    audio, video {
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    
* **audio:not [hidden]**   
R中未指定  


<h2 id="B">Base</h2>

* **html,body**    

N:  
    html {
        font-family: sans-serif; /* 1 */
        -webkit-text-size-adjust: 100%; /* 2 */
        -ms-text-size-adjust: 100%; /* 2 */
    }
    
    body {
        margin: 0;
    }    

R:  

    html, body{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    

<h2 id="L">Link</h2>

a:focus,a:active,a:hover;R中未涉及～  

<h2 id="T">Typography</h2>  

* **h1**  

N:  

    h1 {
      font-size: 2em;
      margin: 0.67em 0;
    }
    
R:  

    h1, h2, h3, h4, h5, h6{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    
* **addr**  

N:

    abbr[title] {
        border-bottom: 1px dotted;
    }
    
R:  

    abbr{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    
    abbr[title], dfn[title] {
       border-bottom:1px dotted #000;
        cursor:help;
    }
    
* **b,strong**  

N:  

    b,strong {
        font-weight: bold;
    }
    
R:  

    b,strong{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }

* **dfn**  

N:  

    dfn {
        font-style: italic;
    }
    
R:  

    dfn {
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    abbr[title], dfn[title] {
        border-bottom:1px dotted #000;
        cursor:help;
    }
    
* **hr**  

N:  

    hr{
        -moz-box-sizing: content-box;
        box-sizing: content-box;
        height: 0;
    }

R:  

    hr {
        display:block;
        height:1px;
        border:0;   
        border-top:1px solid #cccccc;
        margin:1em 0;
        padding:0;
    }
    
* **mark**  

N:  

    mark {
        background: #ff0;
        color: #000;
    }

R:  

    mark {
        background-color:#ff9;
        color:#000; 
        font-style:italic;
        font-weight:bold;
    }
    
* **code,kbd,pre,samp**  

N:

    code,
    kbd,
    pre,
    samp {
        font-family: monospace, serif;
        font-size: 1em;
    }
    pre {
        white-space: pre-wrap;
    }
    
R:  

    code,
    kbd,
    pre,
    samp{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
   }

* **q**  

N:  

    q {
        quotes: "\201C" "\201D" "\2018" "\2019";
    }

R:  

    q{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    q:before, q:after {
        content:'';
        content:none;
    }

* **small**  

N:  

    small {
        font-size: 80%;
    }
    
R:  

    small {
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    
* **sub, sup**  

N:

    sub,
    sup {
        font-size: 75%;
        line-height: 0;
        position: relative;
        vertical-align: baseline;
    }

    sup {
        top: -0.5em;
    }

    sub {
        bottom: -0.25em;
    }
    
R:  

    sub, sup {
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }  
    

<h2 id="E">Embedded content</h2>

* **img**

N:  

    img {
        border: 0;
    }
    
R:  

    img {
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }


* **svg:not(:root)**

未在reset中体现  

<h2 id="F">Figures</h2>  

* **figure**  

N:  

    figure {
        margin: 0;
    }
    
R:  

    figure{ 
      display:block;
    }


<h2 id="Fo">Forms</h2>  

* **fieldset**
N:  

    fieldset {
        border: 1px solid #c0c0c0;
        margin: 0 2px;
        padding: 0.35em 0.625em 0.75em;
    }

R:  

    fieldset{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
    
* **legend**  

N:  

    legend {
        border: 0; /* 1 */
        padding: 0; /* 2 */
    } 
    
R:  

    legend{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }

* **button,input,select,textarea**  

N:  

    button,
    input,
    select,
    textarea {
        font-family: inherit; /* 1 */
        font-size: 100%; /* 2 */
        margin: 0; /* 3 */
    }
    button,input{
        line-height: normal;
    }
    button,select {
        text-transform: none;
    }
    button,
    html input[type="button"], /* 1 */
    input[type="reset"],
    input[type="submit"] {
        -webkit-appearance: button; /* 2 */
        cursor: pointer; /* 3 */
    }
    button[disabled],html input[disabled] {
        cursor: default;
    }
    input[type="checkbox"],input[type="radio"] {
        box-sizing: border-box; /* 1 */
        padding: 0; /* 2 */
    }
    input[type="search"] {
        -webkit-appearance: textfield; /* 1 */
        -moz-box-sizing: content-box;
        -webkit-box-sizing: content-box; /* 2 */
        box-sizing: content-box;
    }
    input[type="search"]::-webkit-search-cancel-button,
    input[type="search"]::-webkit-search-decoration {
        -webkit-appearance: none;
    }
    button::-moz-focus-inner,input::-moz-focus-inner {
        border: 0;
        padding: 0;
    }
    textarea {
        overflow: auto; /* 1 */
        vertical-align: top; /* 2 */
    }
    
    

R:  

    input, select {
        vertical-align:middle;
    }
    input, select {
        vertical-align:middle;
    }


<h2 id="Ta">Tables</h2>

N:  

    table {
        border-collapse: collapse;
        border-spacing: 0;
    }

R:  

    table{
        margin:0;
        padding:0;
        border:0;
        outline:0;
        vertical-align:baseline;
        background:transparent;
    }
