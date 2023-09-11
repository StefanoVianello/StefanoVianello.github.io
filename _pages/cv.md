---
layout: archive
title: "(this page is still under construction)"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}


<!-- <object data="/files/CV_VIANELLO_102021.pdf" type="application/pdf" width="700px" height="700px">
    <embed src="/files/CV_VIANELLO_102021.pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="/files/CV_VIANELLO_102021.pdf">Download PDF</a>.</p>
    </embed>
</object> -->


<!-- https://medium.com/geekculture/33-blog-card-css-for-web-design-726a037217b5 -->
<style>

.projcard-container {
  margin: 50px 0;
}

/* Actual Code: */
.projcard-container,
.projcard-container * {
  box-sizing: border-box;
}
.projcard-container {
  margin-left: auto;
  margin-right: auto;
  width: 1000px;
}
.projcard {
  position: relative;
  width: 100%;
  height: 450px;
  margin-bottom: 40px;
  border-radius: 10px;
  background-color: #fff;
  border: 2px solid #ddd;
  font-size: 18px;
  overflow: hide;
  cursor: pointer;
  box-shadow: 0 4px 21px -12px rgba(0, 0, 0, .66);
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}
.projcard:hover {
  box-shadow: 0 34px 32px -33px rgba(0, 0, 0, .18);
  transform: translate(0px, -3px);
}
.projcard::before {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background-image: linear-gradient(-70deg, #424242, transparent 50%);
  opacity: 0.07;
}
.projcard:nth-child(2n)::before {
  background-image: linear-gradient(-250deg, #424242, transparent 50%);
}
.projcard-innerbox {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
.projcard-img {
  position: absolute;
  height: 300px;
  width: 0px;
  top: 0;
  left: 0;
  transition: transform 0.2s ease;
}
.projcard:nth-child(2n) .projcard-img {
  left: initial;
  right: 0;
}
.projcard:hover .projcard-img {
  transform: scale(1.05) rotate(1deg);
}
.projcard:hover .projcard-bar {
  width: 70px;
}
.projcard-textbox {
  position: absolute;
  top: 7%;
  bottom: 7%;
  left: 60px;
  width: calc(100% - 60px);
  font-size: 17px;
}
.projcard:nth-child(2n) .projcard-textbox {
  left: initial;
  right: 0px;
}
.projcard-textbox::before,
.projcard-textbox::after {
  content: "";
  position: absolute;
  display: none;
  background: #ff0000bb;
  background: #fff;
  top: -20%;
  left: -55px;
  height: 140%;
  width: 60px;
  transform: rotate(8deg);
}
.projcard:nth-child(2n) .projcard-textbox::before {
  display: none;
}
.projcard-textbox::after {
  display: none;
  left: initial;
  right: -55px;
}
.projcard:nth-child(2n) .projcard-textbox::after {
  display: none;
}
.projcard-textbox * {
  position: relative;
}
.projcard-title {
  font-family: 'Voces', 'Open Sans', arial, sans-serif;
  font-size: 24px;
}
.projcard-subtitle {
  font-family: 'Voces', 'Open Sans', arial, sans-serif;
  color: #888;
}
.projcard-bar {
  left: -2px;
  width: 50px;
  height: 5px;
  margin: 10px 0;
  border-radius: 5px;
  background-color: #424242;
  transition: width 0.2s ease;
}
.projcard-blue .projcard-bar { background-color: #0088FF; }
.projcard-blue::before { background-image: linear-gradient(-70deg, #0088FF, transparent 50%); }
.projcard-blue:nth-child(2n)::before { background-image: linear-gradient(-250deg, #0088FF, transparent 50%); }
.projcard-red .projcard-bar { background-color: #D62F1F; }
.projcard-red::before { background-image: linear-gradient(-70deg, #D62F1F, transparent 50%); }
.projcard-red:nth-child(2n)::before { background-image: linear-gradient(-250deg, #D62F1F, transparent 50%); }
.projcard-green .projcard-bar { background-color: #40BD00; }
.projcard-green::before { background-image: linear-gradient(-70deg, #40BD00, transparent 50%); }
.projcard-green:nth-child(2n)::before { background-image: linear-gradient(-250deg, #40BD00, transparent 50%); }
.projcard-yellow .projcard-bar { background-color: #F5AF41; }
.projcard-yellow::before { background-image: linear-gradient(-70deg, #F5AF41, transparent 50%); }
.projcard-yellow:nth-child(2n)::before { background-image: linear-gradient(-250deg, #F5AF41, transparent 50%); }
.projcard-orange .projcard-bar { background-color: #FF5722; }
.projcard-orange::before { background-image: linear-gradient(-70deg, #FF5722, transparent 50%); }
.projcard-orange:nth-child(2n)::before { background-image: linear-gradient(-250deg, #FF5722, transparent 50%); }
.projcard-brown .projcard-bar { background-color: #C49863; }
.projcard-brown::before { background-image: linear-gradient(-70deg, #C49863, transparent 50%); }
.projcard-brown:nth-child(2n)::before { background-image: linear-gradient(-250deg, #C49863, transparent 50%); }
.projcard-grey .projcard-bar { background-color: #424242; }
.projcard-grey::before { background-image: linear-gradient(-70deg, #424242, transparent 50%); }
.projcard-grey:nth-child(2n)::before { background-image: linear-gradient(-250deg, #424242, transparent 50%); }
.projcard-customcolor .projcard-bar { background-color: var(--projcard-color); }
.projcard-customcolor::before { background-image: linear-gradient(-70deg, var(--projcard-color), transparent 50%); }
.projcard-customcolor:nth-child(2n)::before { background-image: linear-gradient(-250deg, var(--projcard-color), transparent 50%); }
.projcard-description {
  z-index: 10;
  font-size: 15px;
  color: #424242;
  height: 250px;
  overflow: auto;
  text-overflow: ellipsis;
}
.projcard-tagbox {
  position: absolute;
  bottom: 3%;
  font-size: 14px;
  cursor: default;
  user-select: none;
  pointer-events: none;
}
.projcard-tag {
  display: inline-block;
  background: #E0E0E0;
  color: #777;
  border-radius: 3px 0 0 3px;
  line-height: 26px;
  padding: 0 10px 0 23px;
  position: relative;
  margin-right: 20px;
  cursor: default;
  user-select: none;
  transition: color 0.2s;
}
.projcard-tag::before {
  content: '';
  position: absolute;
  background: #fff;
  border-radius: 10px;
  box-shadow: inset 0 1px rgba(0, 0, 0, 0.25);
  height: 6px;
  left: 10px;
  width: 6px;
  top: 10px;
}
.projcard-tag::after {
  content: '';
  position: absolute;
  border-bottom: 13px solid transparent;
  border-left: 10px solid #E0E0E0;
  border-top: 13px solid transparent;
  right: -10px;
  top: 0;
}
  </style>




  <div class="projcard-container">
    
  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">
        <div class="projcard-textbox">
        <div class="projcard-title"> Stefano Davide Vianello, PhD</div>
        <div class="projcard-subtitle">ORCID:0000-0002-4152-8990</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"> Postdoctoral researcher, Marine EcoEvoDevo Unit <br/> Current address: 中央研究院所臨海研究站 (Linhai Marine Research Station, Academia Sinica, Taiwan) <br/> <br/>  I am a postdoctoral researcher working in the Marine Eco-Evo-Devo Unit of Prof. Vincent Laudet at the LinHai Marine Research Station, Academia Sinica, Taiwan. My research focuses on the study of gastrointestinal changes during anemonefish metamorphosis, and on the role of thyroid hormones in this process; with a focus on the evolutionary conservation of gastrointestinal metamorphosis mechanisms across deuterostomes. <br/><br/> I completed my PhD in the Laboratory of Stem Cell Engineering of Prof. Matthias Lütolf at EPFL, Switzerland; in which I described the self-organisation properties of endoderm cells as they develop within stem-cell-based models of early embryonic development (gastruloids). I studied Natural Sciences in Cambridge (Girton College), specialising in Genetics. I then worked in the laboratory of Prof. Alfonso Martinez-Arias, Department of Genetics, to investigate the interactions between chemical signalling pathways involved in early embryonic development (Wnt and Notch signalling integration). I am an advocate for intersectional open science, preprinting, and knowledge equity, and a strong critic of the current politics of publishing in academia. Aside from my lab work, I am interested in data communication and visual storytelling in developmental biology.</div>
        <div class="projcard-tagbox">
          <span class="projcard-tag">EcoEvoDevo</span>
          <span class="projcard-tag">endoderm</span>
          <span class="projcard-tag">metamorphosis</span>
          <span class="projcard-tag">gut development</span>
        </div>
      </div>
    </div>
  </div>
  
  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Education</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description">
          <ul>
            <li><span class="projcard-tag">2022-present</span> Marine Research Station, Academia Sinica: Postdoctoral researcher  </li>
            <li><span class="projcard-tag">2017-2021</span> École polytechnique fédérale de Lausanne (EPFL): PhD in Biotechnology and Bioengineering, with Teaching Assistantship</li>
            <li><span class="projcard-tag">2016-2017</span> Girton College, University of Cambridge: MPhil in Biological Science (Genetics) </li>
            <li><span class="projcard-tag">2013-2016</span> Girton College, University of Cambridge: BA Hons Natural Sciences </li>
          </ul>         
        </div>
        </div>
    </div>
  </div>
  
   <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Publications</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"> 
          <ul>
            <li>Suppinger, Zinner, Aizarani, Lukonin, Ortiz, Azzi, Stadler, <b>Vianello</b>, Palla, Kohler, Mayran, Lutolf, Liberali; "Multimodal characterization of murine gastruloid development", 2023</li>
            <li>Tischler, Swank, Hsiung, <b>Vianello</b>, Lutolf, Maerkl; "An automated do-it-yourself system for dynamic stem cell and organoid culture in standard multi-well plates", 2022</li>
            <li><b>Vianello</b>, Lutolf; “In vitro endoderm emergence and self-organisation in the absence of extraembryonic tissues and embryonic architecture”, 2021</li>
            <li><b>Vianello</b>; “Exploring and illustrating the mouse embryo: virtual objects to think and create with”,2020</li>
            <li><b>Vianello</b>, Lutolf; “Understanding the Mechanobiology of Early Mammalian Development through Bioengineered Models”, 2019</li>
          </ul>
        </div>
        </div>
    </div>
  </div>
  
  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Publications</div>
        <div class="projcard-subtitle">Protocols, data, scripts</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"><ul>
            <li><b>Vianello</b>;  “Protocol to process Gastruloids for FACS”. 2021</li>
            <li><b>Vianello</b>, Girgin, Rossi, Lutolf;  “Protocol to generate Gastruloids (LSCB, EPFL)”. 2020</li>
            <li><b>Vianello</b>, Girgin, Rossi, Lutolf;   “Protocol to immunostain Gastruloids (LSCB, EPFL)”. 2020</li>
            <li><b>Vianello</b>, Girgin, Rossi, Lutolf;   “Protocol to culture mESCs (LSCB, UPLUT)”. 2020</li>
            <li><b>Vianello</b>; “RNotebook FACS pipeline”. 2021</li>
            <li><b>Vianello</b>, Sanchez, Bercowsky-Rama, Lutolf; “Gastruloid Intensity Profiler”. 2020</li>
            <li><b>Vianello</b>; “3D models of mouse embryonic development”. 2020</li>
          </ul>
          </div>
        </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Publications</div>
        <div class="projcard-subtitle">Other</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"><ul>
            <li><b>Vianello</b>;   ““English only please!” Real world effects of English-centred literature searches.”. preLights, 2021</li>
            <li><b>Vianello</b>; “Bitter bites for a chocolate lover. Searching for RNAi targets to fight cocoa crop pests”. preLights, 2021</li>
            <li><b>Vianello</b>, Sanchez;  “Say “Aaaah!”. Foregut development and toothed tongues in the black Katy chiton”. preLights, 2021</li>
            <li><b>Vianello</b>, Sanchez; “Navigating change: sentinels of the sea tell about ocean health and disease.”. preLights, 2021</li>
            <li><b>Vianello</b>, Sanchez; “Gastruloids, pescoids, caveoids, surfoids. . . .In vitro embryonic models to study evo-eco-devo. New experimental approaches to cavefish development.”. preLights, 2020</li>
            <li><b>Vianello</b>, Sanchez; “On the (h)edge: the germline precursors of a basal metazoa are induced at the interface between Hedgehog signalling domains”.preLights, 2020</li>
            <li><b>Vianello</b>, Sanchez;  “(Transiently) Comfortable in its own “skin”: formation of epithelium-like multicellular structures in a unicellular organism through conserved actomyosin-dependent mechanisms”. preLights, 2019</li>
            <li><b>Vianello</b>, Sanchez; ; “Mind the gap: epiblast geometry at its extraembryonic boundary constrains BMP localization and ensures robust gradient formation”. preLights, 2019</li>
          </ul>
          <ul>
            <li>"No Diamonds for DevBio", August 2023</li>
            <li>“The “pre” in (my) “preprint” is for pre-figurative”. September 2021</li>
            <li>“Preprint highlighting in a haunted house [Part 1]”. August 2021</li>
          </ul></div>
        </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Posters</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"><ul>
          <li>Jovanic, Godovich, <b>Vianello</b>, Hadjantonakis; International Society for Stem Cell Research Annual meeting, "2D and 3D gastruloid models for investigating mammalian endoderm development" 06.2023 </li>
          <li><b>Vianello</b>, Lutolf; BIRS-CMO WORKSHOP: "MODELLING AND ENGINEERING THE MOUSE EMBRYO" Oaxaca, MX Cancelled due pandemic 04/2020</li>
          <li><b>Vianello</b>, Lutolf; EUROPEAN SUMMER SCHOOL ON STEM CELLS AND REGENERATIVE MEDICINE Hydra, EL "Studying the mechanobiology of early mammalian development using self-organising embryonic organoids" 09/2019</li>
          <li><b>Vianello</b>, Lutolf; EMBO SYMPOSIUM: MECHANICAL FORCES IN DEVELOPMENT Heidelberg, DE "Altering geometry and mechanics to coax the development of self-organising embryonic organoids" 07/2019</li>
          <li><b>Vianello</b>, Lutolf; EMBO SYMPOSIUM: SYNTHETIC MORPHOGENSIS Heidelberg, DE "Altering geometry and mechanics to coax the development of self-organising embryonic organoids" 03/2019</li>
          <li><b>Vianello</b>; EMBO WORKSHOP: VISUALIZING BIOLOGICAL DATA 03/2019</li>
        </ul></div>
        </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Talks</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"><ul>
          <li>ECOEVODEVO INTERGROUP SEMINARS (INTERNAL) Speaker: "Gut metamorphosis in the common clownfish <i>Amphiprion ocellaris</i>", 02.2023</li>
          <li>OASPA Open Access Scholarly Publishing Association Webinar; Invited speaker: "So can publishing respond to a crisis? An evidence-informed approach" 2021</li>
          <li>ASAPbio FELLOWS TRAINING PROGRAMME virtual Invited speaker: "Preprint highlighting in a haunted house: Matthew effect, bias, preprint curation. 2021</li>
          <li> PHYSICS OF LIVING SYSTEMS (INTERNAL) Lausanne, CH "Squeezing, pressing, and bounding Gastruloids: mechanics and symmetry-breaking in vitro. 2019</li>
          <li>EUROTECH SUMMER SCHOOL: OPEN SCIENCE IN PRACTICE Lausanne, CH Invited speaker: “PreLights: a community-driven effort to highlighting preprints. 2019</li>
          <li>EMBO WORKSHOP: IMAGING MOUSE DEVELOPMENT Heidelberg, DE “Elucidating the role of mechanical cues during peri-implantation mouse development”. 2019</li>
        </ul></div>
        </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Community involvement and responsibilities</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"><ul>
          <li>2021: Preprint Curator, Sciety</li>
          <li>2020-2021: Preprint Curator, The company of biologists</li>
          <li>2019-2021: PreLights Contributor, The company of biologists</li>
        </ul></div>
        </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Teaching Training/Experience</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"><ul>
          <li>2021: EPFL ENG-629: LECTURING AND PRESENTING IN ENGINEERING</li>
          <li>2020: EPFL ENG-624: SCIENCE & ENGINEERING TEACHING AND LEARNING</li>
          <li>2021: TEACHING ASSISTANT EPFL BIO-378 PHYSIOLOGY LAB 1</li>
          <li>2018-2021: TEACHING ASSISTANT EPFL BIOENG-110 GENERAL BIOLOGY</li>
          <li>24,25/10/2019: COURSE INSTRUCTOR CAMBIOSCIENCE PRACTICAL COURSE: DISCOVERING GASTRULOIDS</li>
          <li>10/2016; 02/2017: DEMONSTRATOR UNIVERSITY OF CAMBRIDGE</li>
        </ul></div>
        </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Misc</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"> <ul>
          <li><b>Languages</b>: <span class="projcard-tag">Italian (native)</span> <span class="projcard-tag">French (fluent)</span> <span class="projcard-tag">English (fluent)</span> </li>
          <li><b>Affiliations</b>: <span class="projcard-tag">PSDB (Philippine Society for Developmental Biology) member</span>  <span class="projcard-tag">DORA (signatory)</span> </li>
          <li><b>Hobbies</b>: </li>
          <li><b>IT skills</b>: 
            <ul>
              <li><b>Programming</b>: <span class="projcard-tag">R (e.g. Seurat; full scRNAseq and bulkRNAseq analysis, FACS processing)</span> <span class="projcard-tag">Python/Jupyter notebooks</span></li> 
              <li><b>Software</b>: <span class="projcard-tag">MS Office</span> <span class="projcard-tag">LibreOffice</span> <span class="projcard-tag">GIMP/Photoshop</span> <span class="projcard-tag">Inkscape/Adobe Illustrator</span></li>
              <li><b>Web Development</b>: <span class="projcard-tag">PHP</span> <span class="projcard-tag">HTML</span> <span class="projcard-tag">SQL</span> <span class="projcard-tag">CSS</span></li>
              <li><b>Virtual Reality</b>: <span class="projcard-tag">Unity</span> <span class="projcard-tag">Blender</span> <span class="projcard-tag">Google cardboard</span></li>
              <li><span class="projcard-tag">familiarity with Unix environment</span></li>
            </ul>
          </li>
        </ul></div>
        </div>
    </div>
  </div>



</div>