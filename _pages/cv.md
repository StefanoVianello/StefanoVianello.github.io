---
layout: archive
title: ""
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
  width: 100%;
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
        <div class="projcard-subtitle">ORCID iD:<a href="https://orcid.org/0000-0002-4152-8990" target="_blank" rel="noopener noreferrer"> <img alt="ORCID logo" src="https://info.orcid.org/wp-content/uploads/2019/11/orcid_16x16.png" width="16" height="16" /> 0000-0002-4152-8990</a></div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"> Postdoctoral researcher, <a href="https://icob.sinica.edu.tw/Faculty/faculty_lab?id=a6eefa5f952546d9951103c6f9d8cf8b" target="_blank" rel="noopener noreferrer">Marine EcoEvoDevo Unit</a> <br/> Current work address: <a href="https://mrs.icob.sinica.edu.tw/" target="_blank" rel="noopener noreferrer">中央研究院所臨海研究站</a> (Linhai Marine Research Station, Academia Sinica) Taiwan <br/> <br/>  I am a postdoctoral researcher working in the Marine Eco-Evo-Devo Unit of Prof. Vincent Laudet at the LinHai Marine Research Station, Academia Sinica, Taiwan. My research focuses on the study of gastrointestinal changes during anemonefish metamorphosis, and on the role of thyroid hormones in this process; with a focus on the evolutionary conservation of gastrointestinal metamorphosis mechanisms across deuterostomes. <br/><br/> I completed my PhD in the Laboratory of Stem Cell Engineering of Prof. Matthias Lütolf at EPFL, Switzerland; in which I described the self-organisation properties of endoderm cells as they develop within stem-cell-based models of early embryonic development (gastruloids). I studied Natural Sciences in Cambridge (Girton College), specialising in Genetics. I then worked in the laboratory of Prof. Alfonso Martinez-Arias, Department of Genetics, to investigate the interactions between chemical signalling pathways involved in early embryonic development (Wnt and Notch signalling integration). I am an advocate for intersectional open science, preprinting, and knowledge equity, and a strong critic of the current politics of publishing in academia. Aside from my lab work, I am interested in data communication and visual storytelling in developmental biology.</div>
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
        <div class="projcard-title">Education and Professional Experience</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description">
          <ul>
            <li><font style="font-variant: small-caps">2022-present | Marine Research Station, Academia Sinica </font> <br/> <b>Postdoctoral researcher</b> <br/> "Towards an integrated understanding of metamorphosis in bilaterians" <br/> Academia Sinica Grand Challenge Program </li>
            <li><font style="font-variant: small-caps">2017-2021 | École polytechnique fédérale de Lausanne (EPFL)</font> <br/><b>PhD in Biotechnology and Bioengineering</b>, with Teaching Assistantship<br/> Laboratory of Stem Cell Bioengineering, with Prof M. Lütolf <br/> "Endoderm development and morphogenesis in self-organising stem cell-based models of mouse embryogenesis" <br/>  “Characterising the mechanical and geometrical inputs of early mammalian development through bioengineered models of patterning and morphogenesis” <br/>  Swiss National Science Foundation Synergia Grant</li>
            <li><font style="font-variant: small-caps">2016-2017 |  Girton College, University of Cambridge </font> <br/><b>MPhil in Biological Science (Genetics)</b><br/>  “Wnt and Notch (Wntch) interactions in in vitro models of preimplantation embryonic development”, with Prof A. Martinez-Arias</li>
            <li><font style="font-variant: small-caps">2013-2016 |  Girton College, University of Cambridge</font><br/><b> BA Hons Natural Sciences</b></li>
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
            <li>Vianello*, Lin, Pinem, Li, Li, Sonia, Lee, Wu, Laudet, Su, Yu, Schneider; "Deconstructing the common anteroposterior organisation of adult bilaterian guts", 2025 [doi:<a href="https://doi.org/10.1101/2025.07.02.662275">10.1101/2025.07.02.662275</a>]</li>
            <li>Herrera*, <b>Vianello*</b>, Mitchell, Chamot, Lorin-Nebel, Bonnelye, Roux, Besseau, Gibert, Laudet; "From Genes to Pathways: A Curated Gene Approach to Accurate Pathway Reconstruction in Teleost Fish Transcriptomics", 2025 [PMID:<a href="https://doi.org/10.1002/jez.b.23299">40296566</a>], with associated preprint [2024 PPR:<a href="https://doi.org/10.1101/2024.09.23.614382">PPR914795</a>]</li>
            <li>Reynaud*, <b>Vianello*</b>, Lee, Salis, Wu, Frederich, Lecchini, Besseau, Roux, Laudet; "The multi-level effect of chlorpyrifos during clownfish metamorphosis", 2025 [PMID:<a href="https://doi.org/10.1016/j.mce.2025.112535">40187546</a>], with associated preprint [2024 PPR:<a href="https://doi.org/10.1101/2024.08.02.606305">PPR890713</a>] </li>
            <li>Zwahlen, Gairin, <b>Vianello</b>, Mercader, Roux, Laudet; "The ecological function of thyroid hormones", 2024 [PMID:<a href="https://doi.org/10.1098/rstb.2022.0511">38310932</a>]</li>
            <li>Roux, <b>Vianello</b>, Laudet; "Physiology of metamorphosis", 2023 [doi:<a href="https://doi.org/10.1016/B978-0-323-90801-6.00134-8">doi.org/10.1016/B978-0-323-90801-6.00134-8</a>]</li>
            <li>Suppinger, Zinner, Aizarani, Lukonin, Ortiz, Azzi, Stadler, <b>Vianello</b>, Palla, Kohler, Mayran, Lutolf, Liberali; "Multimodal characterization of murine gastruloid development", 2023 [PMID:<a href="https://doi.org/10.1016/j.stem.2023.04.018">37209681</a>]</li>
            <li>Tischler, Swank, Hsiung, <b>Vianello</b>, Lutolf, Maerkl; "An automated do-it-yourself system for dynamic stem cell and organoid culture in standard multi-well plates", 2022 [PMID:<a href="https://doi.org/10.1016/j.crmeth.2022.100244">35880022</a>]</li>
            <li><b>Vianello</b>, Lutolf; “In vitro endoderm emergence and self-organisation in the absence of extraembryonic tissues and embryonic architecture”, 2021 [PPR:<a href="https://doi.org/10.1101/2020.06.07.138883">PPR173378</a>]</li>
            <li><b>Vianello</b>; “Exploring and illustrating the mouse embryo: virtual objects to think and create with”,2020 [PPR:<a href="https://doi.org/10.1101/2020.11.23.393991">PPR243698</a>]</li>
            <li><b>Vianello</b>, Lutolf; “Understanding the Mechanobiology of Early Mammalian Development through Bioengineered Models”, 2019 [PMID:<a href="https://doi.org/10.1016/j.devcel.2019.02.024">30913407</a>]</li>
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
            <li><b>Vianello</b>;  “Protocol to process Gastruloids for FACS”. 2021 [doi:<a href="https://dx.doi.org/10.17504/protocols.io.bvgrn3v6">dx.doi.org/10.17504/protocols.io.bvgrn3v6</a>]</li>
            <li><b>Vianello</b>, Girgin, Rossi, Lutolf;  “Protocol to generate Gastruloids (LSCB, EPFL)”. 2020 [doi:<a href="https://dx.doi.org/10.17504/protocols.io.9j5h4q6">dx.doi.org/10.17504/protocols.io.9j5h4q6</a>]</li>
            <li><b>Vianello</b>, Girgin, Rossi, Lutolf;   “Protocol to immunostain Gastruloids (LSCB, EPFL)”. 2020 [doi:<a href="https://dx.doi.org/10.17504/protocols.io.7tzhnp6">dx.doi.org/10.17504/protocols.io.7tzhnp6</a>]</li>
            <li><b>Vianello</b>, Girgin, Rossi, Lutolf;   “Protocol to culture mESCs (LSCB, UPLUT)”. 2020 [doi:<a href="https://dx.doi.org/10.17504/protocols.io.7xbhpin">dx.doi.org/10.17504/protocols.io.7xbhpin</a>]</li>
            <li><b>Vianello</b>; “RNotebook FACS pipeline”. 2021 <a href="https://doi.org/10.5281/zenodo.4894122"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.4894122.svg" alt="DOI"></a></li>
            <li><b>Vianello</b>, Sanchez, Bercowsky-Rama, Lutolf; “Gastruloid Intensity Profiler”. 2020 <a href="https://doi.org/10.5281/zenodo.4899121"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.4899121.svg" alt="DOI"></a></li>
            <li><b>Vianello</b>; “3D models of mouse embryonic development”. 2020 <a href="https://doi.org/10.5281/zenodo.4284380"><img src="https://zenodo.org/badge/DOI/10.5281/zenodo.4284380.svg" alt="DOI"></a></li>
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
        <div class="projcard-description"><span class="projcard-tag">PreLights posts</span><ul>
            <li><b>Vianello</b>;   ““English only please!” Real world effects of English-centred literature searches.”. preLights, 2021</li>
            <li><b>Vianello</b>; “Bitter bites for a chocolate lover. Searching for RNAi targets to fight cocoa crop pests”. preLights, 2021</li>
            <li><b>Vianello</b>, Sanchez;  “Say “Aaaah!”. Foregut development and toothed tongues in the black Katy chiton”. preLights, 2021</li>
            <li><b>Vianello</b>, Sanchez; “Navigating change: sentinels of the sea tell about ocean health and disease.”. preLights, 2021</li>
            <li><b>Vianello</b>, Sanchez; “Gastruloids, pescoids, caveoids, surfoids. . . .In vitro embryonic models to study evo-eco-devo. New experimental approaches to cavefish development.”. preLights, 2020</li>
            <li><b>Vianello</b>, Sanchez; “On the (h)edge: the germline precursors of a basal metazoa are induced at the interface between Hedgehog signalling domains”.preLights, 2020</li>
            <li><b>Vianello</b>, Sanchez;  “(Transiently) Comfortable in its own “skin”: formation of epithelium-like multicellular structures in a unicellular organism through conserved actomyosin-dependent mechanisms”. preLights, 2019</li>
            <li><b>Vianello</b>, Sanchez; ; “Mind the gap: epiblast geometry at its extraembryonic boundary constrains BMP localization and ensures robust gradient formation”. preLights, 2019</li>
          </ul>
          <span class="projcard-tag">Blogposts</span><ul>
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
        <div class="projcard-title">Talks</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description"><ul>
          <li><b>Speaker</b> | <font style="font-variant: small-caps">Philippine Association of Marine Science 18th National Symposium (PAMS18)</font>: "The multi-level effect of chlorpyrifos during clownfish metamorphosis", scheduled 07.2025</li>
          <li><b>Speaker</b> | <font style="font-variant: small-caps">2025 Joint Conference of the Asian Society of Ichthyologists Annual Meeting and the 12th Indo-Pacific Fish Conference (ASI-IPFC)</font>: "Thyroid hormones trigger stomach differentiation during metamorphosis of the common clownfish (<i>Amphiprion ocellaris</i>)", 06.2025 </li>
          <li><b>Invited speaker</b> | <font style="font-variant: small-caps">University of the Philippines Marine Science Institute (UP MSI) MSI@50 Lecture Series</font>: "Listening to one's gut: approaching marine life evolution, life history transitions, and ecophysiology from the perspective of the gastrointestinal system", 01.2025</li>
          <li><b>Speaker</b> | <font style="font-variant: small-caps">Italian Society of Evolutionary Biology (SIBE)</font>: "Thyroid hormones trigger stomach differentiation during metamorphosis of the common clownfish (<i>Amphiprion ocellaris</i>)", 09.2024</li>
          <li><b>Abstract</b> | <font style="font-variant: small-caps">Italian Zoological Union (UZI)</font>| Celentano (<i>presenter</i>), <b>Vianello</b>, Paradiso, Boriello, Ardizio, Cutignano, Paris, Carbone, Ciavatta, Wu, Lee, Motta, Polese, Mollo, Di Nocera, Laudet: "<i>Amphiprion spp. </i> as a model of aquatic vertebrate nutrition ", 09.2024 | <a href="https://www.uzionlus.it/83-congresso-uzi-2024/Book_Abstracts_Posters.pdf"> Abstract booklet </a> </li>
          <li><b>Invited Speaker</b> | <font style="font-variant: small-caps">OIST-CNRS Joint Symposium on West Pacific Marine Biology</font>: "Thyroid hormones trigger stomach development and differentiation during clownfish metamorphosis", 07.2024</li>
          <li><b>Accepted for talk</b> | <font style="font-variant: small-caps">EuroEvoDevo 2024: Meeting of the European Evolutionary Developmental Biology Society, Fish Satellite Meeting</font>: "Thyroid hormones trigger stomach differentiation during metamorphosis of the common clownfish (<i>Amphiprion ocellaris</i>)", 06.2023 *(could not attend)*</li>
          <li><b>Speaker</b> | <font style="font-variant: small-caps">EcoEvoDevo Intergroup Seminars (internal)</font>: "Gut metamorphosis in the common clownfish <i>Amphiprion ocellaris</i>", 02.2023</li>
          <li><b>Invited speaker</b> | <font style="font-variant: small-caps">International Science Council: Open Science South Asian Network Conference 2022</font>: "Preprints- A Pathway to Open Access", 09.2022</li>
          <li><b>Invited speaker</b> | <font style="font-variant: small-caps">eLife Early Career Researcher Wednesday Webinar Series</font>: "Do-it-Yourself strategies to prefigurative publishing", 05.2022</li>
          <li><b>Invited speaker</b> | <font style="font-variant: small-caps">OASPA Open Access Scholarly Publishing Association Webinar</font>: "So can publishing respond to a crisis? An evidence-informed approach" 12.2021</li>
          <li><b>Invited speaker</b> | <font style="font-variant: small-caps">Preprints in Motion Podcast</font>: "Be the change you want to see: Prefigurative politics in academia" 11.2021</li>
          <li><b>Invited speaker</b> (virtual) | <font style="font-variant: small-caps">ASAPbio Fellows Training Programme</font>: "Preprint highlighting in a haunted house: Matthew effect, bias, preprint curation. 2021</li>
          <li><b>Speaker</b> | <font style="font-variant: small-caps"> Physics of Living Systems (internal)</font>: "Squeezing, pressing, and bounding Gastruloids: mechanics and symmetry-breaking in vitro. 2019</li>
          <li><b>Invited speaker</b> | <font style="font-variant: small-caps">Eurotech Summer School: Open Science in Practice</font>: "PreLights: a community-driven effort to highlighting preprints". 2019</li>
          <li><b>Speaker</b> | <font style="font-variant: small-caps">EMBO Workshop: Imaging mouse development</font>: "Elucidating the role of mechanical cues during peri-implantation mouse development". 2018</li>
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
          <li><b>Vianello</b>, Lee, Wu, Roux, Laudet; <font style="font-variant: small-caps"> Institute of Cellular and Organismic Biology (ICOB) departmental poster presentation </font>, "Thyroid hormones trigger the appearance and differentiation of the stomach during the metamorphosis ofthe common clownfish (Amphiprion ocellaris)" | 11.2023 | [doi:<a href="https://doi.org/10.6084/m9.figshare.24457543.v1">doi.org/10.6084/m9.figshare.24457543.v1</a>] </li>
          <li>Jovanic, Godovich, <b>Vianello</b>, Hadjantonakis; <font style="font-variant: small-caps"> International Society for Stem Cell Research (ISSCR) annual meeting </font>, "2D and 3D gastruloid models for investigating mammalian endoderm development" | 06.2023 | Abstract booklet <a href="https://static1.squarespace.com/static/611faaa8fee682525ee16489/t/64ac79566a2d4b5430e9b891/1689024858598/ISSCR+2023+Abstract+Book.pdf"> number 467</a> </li>
          <li><b>Vianello</b>, Lutolf; <font style="font-variant: small-caps"> BIRS-CMO Workshop: "Modelling and engineering the mouse embryo" Oaxaca, MX </font> | Cancelled due pandemic 04.2020</li>
          <li><b>Vianello</b>, Lutolf; <font style="font-variant: small-caps">European Summer School on Stem Cells and Regenerative Medicine Hydra, EL </font>, "Studying the mechanobiology of early mammalian development using self-organising embryonic organoids" |09.2019</li>
          <li><b>Vianello</b>, Lutolf; <font style="font-variant: small-caps"> EMBO Symposium: Mechanical Forces in Development Heidelberg, DE </font>, "Altering geometry and mechanics to coax the development of self-organising embryonic organoids" | 07.2019</li>
          <li><b>Vianello</b>, Lutolf;<font style="font-variant: small-caps"> EMBO Symposium: Synthetic Morphogenesis Heidelberg, DE </font>, "Altering geometry and mechanics to coax the development of self-organising embryonic organoids" 03.2019</li>
          <li><b>Vianello</b>;<font style="font-variant: small-caps"> EMBO Workshop: Visualizing Biological Data </font> | 03.2019</li>
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
          <li>2025: <b>Organising Committee</b>: Satellite Meeting of the 2025 Joint Conference of the Asian Society of Ichthyologists Annual Meeting and the 12th Indo-Pacific Fish Conference (ASI-IPFC) </li>
          <li>2021: <b>Preprint Curator</b>, Sciety</li>
          <li>2020-2021: <b>Preprint Curator</b>, The company of biologists</li>
          <li>2019-2021: <b>PreLights Contributor</b>, The company of biologists</li>
        </ul></div>
        </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">     
      <div class="projcard-textbox">
        <div class="projcard-title">Teaching Training/Experience</div>
        <div class="projcard-bar"></div>
        <div class="projcard-description">
        Teaching experience:
        <ul>
          <li>2025: <b>Supervisor</b>: Bachelor Research Student internship (4 months)</li>
          <li>2024: <b>Supervisor</b>: Research Secondment PhD student (3 months) </li>          
          <li>2021: <b>Teaching Assistant</b> <font style="font-variant: small-caps">EPFL BIO-378</font>: Physiology Lab 1</li>
          <li>2018-2021: <b>Teaching Assistant</b> <font style="font-variant: small-caps">EPFL BIOENG-110</font>: General Biology</li>
          <li>24,25/10/2019: <b>Course Instructor</b> <font style="font-variant: small-caps">CamBioscience</font>: Practical Course: Discovering Gastruloids</li>
          <li>10/2016; 02/2017: <b>Demonstrator</b> <font style="font-variant: small-caps">University of Cambridge</font></li>
        </ul>
        Teaching training:
          <ul>
          <li>2024: <font style="font-variant: small-caps">University of the Philippines Center for Integrative and Development Studies (UP CIDS)</font>: International Conference "Resisting Intellectual Imperialism and Epistemic Violence: Towards Autonomous Knowledge Production"</li>
          <li>2021: <font style="font-variant: small-caps">EPFL ENG-629</font>: Lecturing and presenting in engineering</li>
          <li>2020: <font style="font-variant: small-caps">EPFL ENG-624</font>: Science and Engineering Teaching and Learning</li>
          
        </ul>
        </div>
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
          <li><b>Affiliations</b>: <span class="projcard-tag">PSDB (Philippine Society for Developmental Biology) member</span> <span class="projcard-tag">TSDB (Taiwanese Society of Developmental Biology) member</span> <span class="projcard-tag">DORA (signatory)</span> <span class="projcard-tag">IUS (International Union of Scientists Against Militarism and the Destructive Use of Science) member</span> </li>
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