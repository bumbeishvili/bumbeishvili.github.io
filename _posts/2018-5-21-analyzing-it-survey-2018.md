---
comments: true
issurvey2018: true
title: Georgian IT Survey 2018
language:   Georgian Language
subtitle: 'd3.js'
date: 2018-05-21 00:00:00
description: This page is a demo that shows everything you can do inside portfolio and blog posts.
featured_image: '/images/blogs/observable/avg-salary.png'
---
<style>
.observable-wrapper svg{
  display:block;
  margin: 0 auto;
}


.observable-wrapper {
    margin-bottom: 15px;
}

.dc-wrapper-second{
    width:102%;
}

.observable-wrapper h1{
   margin-top: 60px;
   margin-bottom: 55px;
}

.observable-wrapper h2{
   margin-top: 60px;
   margin-bottom: 55px;
}

.observable-wrapper h3{
   margin-top: 60px;
   margin-bottom: 55px;
}

.observablehq--boolean{
    display:none;
}

.single h1, .single h2, .single h3, .single h4, .single h5, .single h6, .single p, .single ul, .single ol {
    max-width: 80% !important; 
}

input {
  -webkit-appearance: checkbox;
      margin-left: 10%;
}
#DIV_1{
   margin: 0 auto !important;
}

ul, ol {
    list-style-position: initial !important;
}

</style> 



<div class="full-page-blog-width">

</div>

<script type="module">

  import notebook from "https://api.observablehq.com/@bumbeishvili/how-much-georgian-devs-earn.js";



document.querySelector('.full-page-blog-width').innerHTML = notebook.modules[0].variables
.filter(d=>d)
.map((d,i)=>` <div class="observable-wrapper div-number-${i}" 
               ${i>62?"style='display:none'":''}></div>`)
.join('')



  import {Inspector, Runtime} from "https://unpkg.com/@observablehq/notebook-runtime@1.2.0?module";
 
 

   let i=1;
   Runtime.load(notebook, (variable) => {
       console.log(variable.name=='ოფისში_მომუშავეები'?variable:'')

      return new Inspector(document.querySelector(`.observable-wrapper:nth-child(${i++})`));
   });

</script>