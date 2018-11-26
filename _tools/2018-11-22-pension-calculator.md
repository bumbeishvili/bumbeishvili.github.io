---
layout: tool
comments: true
title: Pension calculator
language:   Georgian Language
subtitle: 'd3.js'
date: 2018-11-21 00:00:00
description: This page is a demo that shows everything you can do inside portfolio and blog posts.
featured_image: '/images/tools/pension.png'
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



.single h1, .single h2, .single h3, .single h4, .single h5, .single h6, .single p, .single ul, .single ol {
    max-width: 80% !important; 
}

input {
  -webkit-appearance: initial;
 
}


ul, ol {
    list-style-position: initial !important;
}

.observablehq--inspect{
  display:none
}
 input[type=range] {
  box-sizing: border-box;
  font-size: 16px;
  line-height: 1;
  height: 2em;
  background-color: transparent;
  cursor: pointer;
  -webkit-appearance: none;
  width: 100%;
}
input[type=range]::-webkit-slider-thumb {
  -webkit-appearance: none;
}
input[type=range]:focus {
  outline: none;
}
input[type=range]::-ms-track {
  width: 100%;
  cursor: pointer;
  background: transparent;
  border-color: transparent;
  color: transparent;
}
input[type=range]::-webkit-slider-thumb {
  -webkit-appearance: none;
  width: 2em;
  height: 2em;
  margin-top: 0;
  background-color: #16a085;
  border-radius: 1em;
  border: 2px solid rgba(255, 255, 255, 0.5);
  cursor: pointer;
}
input[type=range]::-moz-range-thumb {
  width: 2em;
  height: 2em;
  margin-top: 0;
  background-color: #16a085;
  border-radius: 1em;
  border: 2px solid rgba(255, 255, 255, 0.5);
  cursor: pointer;
}
input[type=range]::-ms-thumb {
  width: 2em;
  height: 2em;
  margin-top: 0;
  background-color: #16a085;
  border-radius: 1em;
  border: 2px solid rgba(255, 255, 255, 0.5);
  cursor: pointer;
}
input[type=range]:hover::-webkit-slider-thumb {
  border-color: rgba(255, 255, 255, 0.7);
}
input[type=range]:hover::-moz-range-thumb {
  border-color: rgba(255, 255, 255, 0.7);
}
input[type=range]:hover::-ms-thumb {
  border-color: rgba(255, 255, 255, 0.7);
}
input[type=range]:active::-webkit-slider-thumb {
  border-color: #ffffff;
}
input[type=range]:active::-moz-range-thumb {
  border-color: #ffffff;
}
input[type=range]:active::-ms-thumb {
  border-color: #ffffff;
}
input[type=range]::-webkit-slider-runnable-track {
  width: 100%;
  cursor: pointer;
  height: 1em;
  border-bottom: 2px solid rgba(255, 255, 255, 0.5);
  background-color: transparent;
}
input[type=range]::-moz-range-track {
  width: 100%;
  cursor: pointer;
  height: 1em;
  border-bottom: 2px solid rgba(255, 255, 255, 0.5);
  background-color: transparent;
}
input[type=range]::-ms-track {
  background: transparent;
  border-color: transparent;
  color: transparent;
}
section {
  display: flex;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #16a085;
}
section div {
  margin: auto;
  width: 80%;
}
section h1 {
  font-family: "Helvetica Neue", Helvetical, Arial, sans-serif;
  font-weight: 300;
  margin-bottom: 100px;
  text-align: center;
  font-size: 42px;
  color: rgba(0, 0, 0, 0.3);
}
.block{
  display:inline-block;
  width:49%;
  padding:5px;
  float:left;
}


/*!
// CSS only Responsive Tables
// http://dbushell.com/2016/03/04/css-only-responsive-tables/
// by David Bushell
*/

.rtable {
  /*!
  // IE needs inline-block to position scrolling shadows otherwise use:
  // display: block;
  // max-width: min-content;
  */
  display: inline-block;
  vertical-align: top;
  max-width: 100%;
  
  overflow-x: auto;
  
  // optional - looks better for small cell values
  white-space: nowrap;

  border-collapse: collapse;
  border-spacing: 0;
}

.rtable,
.rtable--flip tbody {
  // optional - enable iOS momentum scrolling
  -webkit-overflow-scrolling: touch;
  
  // scrolling shadows
  background: radial-gradient(left, ellipse, rgba(0,0,0, .2) 0%, rgba(0,0,0, 0) 75%) 0 center,
              radial-gradient(right, ellipse, rgba(0,0,0, .2) 0%, rgba(0,0,0, 0) 75%) 100% center;
  background-size: 10px 100%, 10px 100%;
  background-attachment: scroll, scroll;
  background-repeat: no-repeat;
}

// change these gradients from white to your background colour if it differs
// gradient on the first cells to hide the left shadow
.rtable td:first-child,
.rtable--flip tbody tr:first-child {
  background-image: linear-gradient(to right, rgba(255,255,255, 1) 50%, rgba(255,255,255, 0) 100%);
  background-repeat: no-repeat;
  background-size: 20px 100%;
}

// gradient on the last cells to hide the right shadow
.rtable td:last-child,
.rtable--flip tbody tr:last-child {
  background-image: linear-gradient(to left, rgba(255,255,255, 1) 50%, rgba(255,255,255, 0) 100%);
  background-repeat: no-repeat;
  background-position: 100% 0;
  background-size: 20px 100%;
}

.rtable th {
  font-size: 11px;
  text-align: left;
  background: #f2f0e6;
}

.rtable th,
.rtable td {
  padding: 6px 12px;
  border: 1px solid #d9d7ce;
}

.rtable--flip {
  display: flex;
  overflow: hidden;
  background: none;
}

.rtable--flip thead {
  display: flex;
  flex-shrink: 0;
  min-width: min-content;
}

.rtable--flip tbody {
  display: flex;
  position: relative;
  overflow-x: auto;
  overflow-y: hidden;
}

.rtable--flip tr {
  display: flex;
  flex-direction: column;
  min-width: min-content;
  flex-shrink: 0;
}

.rtable--flip td,
.rtable--flip th {
  display: block;
}

.rtable--flip td {
  background-image: none !important;
  // border-collapse is no longer active
  border-left: 0;
}

// border-collapse is no longer active
.rtable--flip th:not(:last-child),
.rtable--flip td:not(:last-child) {
  border-bottom: 0;
}






.dropdown  select{
  display: inline-block;
  position: relative;
  overflow: hidden;
  height: 28px;
  width: 208px;
  background: #f2f2f2;
  border: 1px solid;
  border-color: white #f7f7f7 whitesmoke;
  border-radius: 3px;
  background-image: -webkit-linear-gradient(top, transparent, rgba(0, 0, 0, 0.06));
  background-image: -moz-linear-gradient(top, transparent, rgba(0, 0, 0, 0.06));
  background-image: -o-linear-gradient(top, transparent, rgba(0, 0, 0, 0.06));
  background-image: linear-gradient(to bottom, transparent, rgba(0, 0, 0, 0.06));
  -webkit-box-shadow: 0 1px 1px rgba(0, 0, 0, 0.08);
  box-shadow: 0 1px 1px rgba(0, 0, 0, 0.08);
}

.dropdown select:before, .dropdown select:after {
  content: '';
  position: absolute;
  z-index: 2;
  top: 9px;
  right: 10px;
  width: 0;
  height: 0;
  border: 4px dashed;
  border-color: #888888 transparent;
  pointer-events: none;
}

.dropdown select:before {
  border-bottom-style: solid;
  border-top: none;
}

.dropdown select:after {
  margin-top: 7px;
  border-top-style: solid;
  border-bottom: none;
}

.dropdown-select select{
  position: relative;
  width: 130%;
  margin: 0;
  padding: 6px 8px 6px 10px;
  height: 28px;
  line-height: 14px;
  font-size: 12px;
  color: #62717a;
  text-shadow: 0 1px white;
  background: #f2f2f2; /* Fallback for IE 8 */
  background: rgba(0, 0, 0, 0) !important; /* "transparent" doesn't work with Opera */
  border: 0;
  border-radius: 0;
  -webkit-appearance: none;
}

.dropdown-select select:focus {
  z-index: 3;
  width: 100%;
  color: #394349;
  outline: 2px solid #49aff2;
  outline: 2px solid -webkit-focus-ring-color;
  outline-offset: -2px;
}

.dropdown-select select > option {
  margin: 3px;
  padding: 6px 8px;
  text-shadow: none;
  background: #f2f2f2;
  border-radius: 3px;
  cursor: pointer;
}

/* Fix for IE 8 putting the arrows behind the select element. */

.lt-ie9 .dropdown {
  z-index: 1;
}

.lt-ie9 .dropdown-select {
  z-index: -1;
}

.lt-ie9 .dropdown-select:focus {
  z-index: 3;
}

/* Dirty fix for Firefox adding padding where it shouldn't. */

@-moz-document url-prefix() {
  .dropdown-select {
    padding-left: 6px;
  }
}

input[type=range]::-webkit-slider-runnable-track {
  /* width: 100%;
  height: 8.4px;
  cursor: pointer;
  box-shadow: 1px 1px 1px #000000, 0px 0px 1px #0d0d0d;
  background: #3071a9;
  border-radius: 1.3px;
  border: 0.2px solid #010101; */
  
  border-bottom: 2px solid #00A586;
}

input[type=range]::-moz-range-track {

  border-bottom: 2px solid #00A586;
  margin-top:5px;
}

.div-number-14{
  display:inline;
}
.div-number-15{
      display: inline-block;
    width: 65%;
}
.widgets{
   width:33%;
   display:inline-block;
}
.widget{
  text-align:center;
  /* display:inline-block; */
  width:100%;
  background:#00A586;
  padding-top:20px;
   padding-bottom:20px;
   color:white;
   min-height:125px;
   float:left;
   margin-left:5px;
   margin-bottom:5px;
}

.widget div{
  margin-bottom:10px;
}

.widget .number{
  font-size:40px;
}

.pension-wrapper{
  padding:20px;
}


@media screen and (max-width: 900px) {
  table{
    width:50% !important;
  }
  .widgets{
     width:100%;
  }
  .div-number-14{
  display:inline-block;
}
  .widget .number{
    
   }

   .widget{
      margin-left:2px !important;
   }
   .block{
     width:90%;
   }
}
</style> 
<div class='pension-wrapper'>
<div id="fb-root"></div>
 <div class='observable-wrapper div-number-1'>
</div>
<div>
<div class='block'>
  <div class='observable-wrapper div-number-2'>
  </div>
  <div class='observable-wrapper div-number-3'>
  </div>
 </div>

 <div class='block'>
  <div class='observable-wrapper div-number-5'>
  </div>
  <div class='observable-wrapper div-number-6'>
  </div>
 </div>

 <div class='block'>
  <div class='observable-wrapper div-number-8'>
  </div>
  <div class='observable-wrapper div-number-9'>
  </div>
 </div>


 <div class='block'>
  <div class='observable-wrapper div-number-11'>
  </div>
  <div class='observable-wrapper dropdown div-number-12'>
  </div>
 </div>
</div>

<div class="full-page-blog-width" style="clear:both">
 

</div>
<br/><br/>
<a href='https://beta.observablehq.com/@bumbeishvili/pension-calculator/2'>იმპლემენტაციის დეტალების ნახვა ამ <b>ნოუთბუქში </b>შეგიძლიათ  </a>

<br/><br/><br/><br/>


<div class="fb-share-button" data-href="https://bumbeishvili.github.io/tools/pension-calculator" data-layout="button_count" data-size="large" data-mobile-iframe="true"><a target="_blank" href="https://www.facebook.com/sharer/sharer.php?u=https%3A%2F%2Fbumbeishvili.github.io%2Ftools%2Fpension-calculator&amp;src=sdkpreparse" class="fb-xfbml-parse-ignore">Share</a></div>
</div>
<div style='display:none' data-type='module' class='script-this'>
    
 console.log('start')
  import notebook from "https://api.observablehq.com/@bumbeishvili/pension-calculator/2.js";

console.log('imported')

const html = document.querySelector('.full-page-blog-width').innerHTML;
document.querySelector('.full-page-blog-width').innerHTML=(html+notebook.modules[0].variables
.filter(d=>d)
.map((d,i)=>{
  if(i<7) return '';
  return ` <d`+`iv class="observable-wrapper div-number-${i}" 
               ${i>=21?"style='display:none'":''}></`+`div>`
})
.join(''));

console.log('created')


  import {Inspector, Runtime} from "https://unpkg.com/@observablehq/notebook-runtime@1.2.0?module";
 
 

   let i=1;
   Runtime.load(notebook, (variable) => {
       const selector = `.observable-wrapper.div-number-${i++}`
       if(document.querySelector(selector)){
      return new Inspector(document.querySelector(selector));
       }

   });

console.log('finished');


   
</div>
 

<script>

     s = document.createElement('script');
    s.type = 'module';
    var code = document.querySelector('.script-this').innerText;
    try {
      s.appendChild(document.createTextNode(code));
      document.body.appendChild(s);
    } catch (e) {
      s.text = code;
      document.body.appendChild(s);
}

 </script>