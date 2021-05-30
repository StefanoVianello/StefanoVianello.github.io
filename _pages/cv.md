---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<style>
  #pdf-viewer {
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.1);
    overflow: auto;
  }

  .pdf-page-canvas {
    display: block;
    margin: 5px auto;
    border: 1px solid rgba(0, 0, 0, 0.2);
  }
</style>

<script>   
    url = 'https://github.com/mozilla/pdf.js/blob/master/test/pdfs/tracemonkey.pdf';
    var thePdf = null;
    var scale = 1;

    PDFJS.getDocument(url).promise.then(function(pdf) {
        thePdf = pdf;
        viewer = document.getElementById('pdf-viewer');

        for(page = 1; page <= pdf.numPages; page++) {
          canvas = document.createElement("canvas");    
          canvas.className = 'pdf-page-canvas';         
          viewer.appendChild(canvas);            
          renderPage(page, canvas);
        }
    });

    function renderPage(pageNumber, canvas) {
        thePdf.getPage(pageNumber).then(function(page) {
          viewport = page.getViewport(scale);
          canvas.height = viewport.height;
          canvas.width = viewport.width;          
          page.render({canvasContext: canvas.getContext('2d'), viewport: viewport});
    });
    }
</script>

<div id='pdf-viewer'></div>
