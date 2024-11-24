---
layout: archive
title: "Research Projects"
permalink: /research_intro/
author_profile: true
---

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
  height: 1100px;
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
  height: 800px;
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

 <b>Postdoctoral research </b> 

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">
        <div class="projcard-textbox">
        <div class="projcard-title"> Gut metamorphosis in the common clownfish</div>
        <!-- <div class="projcard-subtitle">Gut metamorphosis in the common clownfish</div> -->
        <div class="projcard-bar"></div>
        <div class="projcard-description"> I study the hormonal control of metamorphosis in the common clownfish (<i>Amphiprion ocellaris</i>). Specifically, I focus on the transformations in gastrointestinal anatomy and function as the larvae undergo the broader metamorphic changes that prepare them to settle in the reef.  <br/> <img src="https://StefanoVianello.github.io/images/metamorphosis_Aocellaris.png" alt="Diagram of the common clownfish lifecycle between pelagic larval life and settlement into the reef"><figcaption> Illustration of the lifecycle of the common clownfish. Larvae (rightmost) disperse into the ocean (pelagic phase). Major physiological, behavioral, and ecological changes (metamorphosis) take place as the larval body plan is recruited into the reef and the clownfish finds an anemome in which to house. Figure redrawn from (<a href="https://doi.org/10.1002/dvdy.46">Roux et al. 2019</a>). <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a> Image licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>. </figcaption></div>
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
        <div class="projcard-title"> Endocrine disrupting effects of organophosphate pesticides</div>
        <div class="projcard-subtitle">using clownfish as a laboratory model</div>
        <div class="projcard-bar"> </div>
        <div class="projcard-description"> Read the preprint at: <a href="https://www.biorxiv.org/content/10.1101/2024.08.02.606305v2"><b>Reynaud</b>, <b>Vianello</b> <i>et al</i>., "The multi-level effect of chlorpyrifos during clownfish metamorphosis" (2024). </a><br/> <font color="gray"> A collaboration with Dr. Matthieu Reynaud. Pharmacological perturbation, transcriptomics, fish phisiology. The collaboration is <b>still ongoing</b> with more data and an extension of the ecotoxicological relevance of the study. </font> <br/> <br/>
        
        
        Chlorpyrifos is an organophosphate pesticide widely used in agriculture: classified as a persitant organic polluter, it leaches into the soil and waterstreams following application, and accumulates long-term within coastal marine sediments. Its use has bee long associated with the violation of labour- and human rights in both Southeast Asia and South America, backed at least in part by neocolonial EU trade policies. In Taiwan, the use of Chlorpyrifos (陶斯松) is under <a href="https://www.moenv.gov.tw/en/6F017386BDF4CDF5/4d875576-a2a3-4c57-ba2a-348b04833a2b">ongoing phaseout</a>, with a total ban planned <a href="https://www.taipeitimes.com/News/taiwan/archives/2022/03/07/2003774336"> by 2026 </a>. Within South East Asia, its use has been officially banned in <a href="https://panap.net/2022/08/malaysia-commended-for-ban-on-chlorpyrifos-and-carbofuran/">Malaysia</a>, <a href="https://panap.net/2019/02/pan-vietnam-welcomes-the-ban-of-chlorpyrifos-and-fipronil/">Vietnam</a>, and <a href="https://www.ratchakitcha.soc.go.th/DATA/PDF/2563/E/117/T_0056.PDF">Thailand</a>, though <a href="https://fpa.da.gov.ph/call-to-ban-chlorpyrifos-application-in-banana-raised-to-extruders-in-davao/">not yet in the Philippines</a> and <a href="https://ipen.org/documents/situation-report-chlorpyrifos-indonesia"> Indonesia</a>, despite this pesticide having such "significant adverse human health and/or environmental effects, that global action is warranted" according to the latest <a href="https://www.pops.int/TheConvention/POPsReviewCommittee/Meetings/POPRC20/Overview/tabid/9850/Default.aspx">Stockholm Convention's Persistent Organic Pollutants Review Committee review </a>. <br/> <br/>
        
        <b>Particular alarm and morbidity has always concerned the effects of Chlorpyrifos as an endocrine disruptor</b>, including on the Thyroid Hormone Axis. By using metamorphosing larvae of the common clownfish <i> Amphiprion ocellaris </i> as a model system of Thyroid Hormone endocrine regulation in fish, we characterised the effect of this pesticide on a marine fish at the level of the whole transcriptome, with a further focus on the consequences on the Thyroid Hormone endocrine axis. Beside the ecotoxicological inferences that this research allows, specifically on the threat represented by transmaritime trade across tropical waters, our findings provide one of the first system-level description of the potential effects of this pesticide on fish, and in comparison to known thyroid hormone axis modulators. <br/>
        <img src="https://StefanoVianello.github.io/images/chlorpyrifosspray.png" alt="Farmers spraying chlorpyrifos pesticide on crops">
        </div>
        <div class="projcard-tagbox">
          <span class="projcard-tag">EcoDevo</span>
          <span class="projcard-tag">Pesticides</span>
          <span class="projcard-tag">metamorphosis</span>
          <span class="projcard-tag">Endocrine disruption</span>
        </div>
      </div>
    </div>
  </div>

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">
        <div class="projcard-textbox">
        <div class="projcard-title"> Effect of dietary phytochemicals on coral reef biology</div>
        <!-- <div class="projcard-subtitle">Effect of chlorpyrifos on clownfish metamorphosis</div> -->
        Species of the genus <i>Caulerpa</i>, a siphonaceous green alga that grows in the upper sublittoral zone of tropical coral reefs,  are widely distributed in Australian and Southeast Asian waters. <i>Caulerpa lentillifera</i> and varieties of <i>Caulerpa racemosa</i> are for example considered a delicacy in the Philippines, Indonesia, Malaysia, and Okinawa (Japan), and many <i>Caulerpa</i> species have (also) been long valued for their medicinal uses. In fact, <i>Caulerpa</i> varieties are now widely farmed in many Southeast Asian nations, a practice first developed in the 1950s in Mactan Island, Cebu (Philippines). <br/> <br/>

On the other hand, a member of the <i>Caulerpa racemosa</i> complex is currently a source of heightened concern in the Mediterranean Sea, new waters it is believed to have reached as a result of aquarium trade from Western Australia. In these waters, in the form of the so-called <i>var. cylindracea</i>, this species has shown one of the highest invasive characters ever recorded in the Mediterranean, affecting pre-established seagrass ecosystems and reducing species diversity. Further concern has notably derived from its accumulation within the tissues of local sparid species of human consumption (e.g.  <i>Diplodus sargus</i>). <br/> <br/>

Critically, <i>Caulerpa cylindracea</i> and many other species of the genus synthesize a bisindolic red pigment called caulerpin, first discovered in Caulerpa racemosa by Filipino scientist Gertrudes Aguilar Santos. While data on the accumulation of this compound in fish of historical <i>Caulerpa spp.</i> tropical habitats are difficult to find, an increasing body of literature has instead documented its clear accumulation in muscle and liver of Mediterranean species, and its effects on fish physiology have been characterised in terms of restricted panels of expected mechanisms of action (notably, oxidative stress; refs).
        
        <div class="projcard-bar"></div>
        <div class="projcard-description"> </div>
        <div class="projcard-tagbox">
          <span class="projcard-tag">EcoEvoDevo</span>
          <span class="projcard-tag">endoderm</span>
          <span class="projcard-tag">metamorphosis</span>
          <span class="projcard-tag">gut development</span>
        </div>
      </div>
    </div>
  </div>

<b>PhD research</b> 

  <div class="projcard projcard-grey">
    <div class="projcard-innerbox">
        <div class="projcard-textbox">
        <div class="projcard-title"> Endoderm development in gastruloids</div>
        <!-- <div class="projcard-subtitle">Endoderm development in gastruloids</div> -->
        <div class="projcard-bar"></div>
        <div class="projcard-description"> In humans, mice, and other mammals key internal organs such as the gut, lungs, pancreas, liver, thyroid, thymus, and bladder (and many others!) all derive from the same embryonic tissue: the endoderm. The development of all of these structures thus depends on a same set of early cells, and on the developmental instructions provided to them by the embryo. To study what these instructions might be, I am currently investigating the modes of development that endoderm cells (and their progenitors) execute when they can <i>not</i> rely on them. That is, when they are made to self-organise <i>in vitro</i> in a dish in the lab. Even on their own, endoderm cells emerge with timings and patterns comparable to what happens when they are on the embryo, and eventually form patterned structures in many way similar to the embryonic gut tube. My research touches on topics of endoderm and epithelial identity, self-organisation, patterning, and fundamental mammalian developmental biology. <br/> <img src="https://StefanoVianello.github.io/images/TBra_foxA2_banner.PNG" alt="Gastruloids immunostained for endoderm marker FoxA2 and posterior marker TBra"><figcaption> Embryonic stem cells can be left to self-organise into structures called Gastruloids. These provide an <i>in vitro</i> model of embryonic development. Endoderm cells, marked here in cyan (FoxA2), form an elongated internal core. The posterior marker TBra (gold) marks the posterior of the aggregate. </figcaption> <br/> <img src="https://StefanoVianello.github.io/images/Gastruloids_and_tail.PNG" alt="Gastruloids next to the tailbud of a mouse embryo. The same makers have been immunostained in both."><figcaption> Gastruloids have been found to express genes in a organised way, in many way similar (and in many ways different) from that of the real mouse embryo. In the image above, the same markers have been stained in the tail of a mouse embryo (big structure on the right) and in 7-days-old Gastruloids. Insight comes from the comparison between what seen in the embryo and what observed to happen in these self-organising *in vitro* systems. </figcaption> <br/> <img src="https://StefanoVianello.github.io/images/Gastruloid_quantification.PNG" alt="Plots showing alternative quantifications of the marker expression patterns in Gastruloids"><figcaption> The patterns of gene expression amongst Gastruloids are very robust and reproducible. We can image entire populations of Gastruloids and extract spatial information about where specific genes are expressed along the main axis. </figcaption></div>
        <div class="projcard-tagbox">
          <span class="projcard-tag">gastruloids</span>
          <span class="projcard-tag">endoderm</span>
          <span class="projcard-tag">embryonic stem cells</span>
        </div>
      </div>
    </div>
  </div>
</div>

<!--
## Research Projects

**Postdoc research** <br/>
I study the hormonal control of metamorphosis in the common clownfish (*Amphiprion ocellaris*). Specifically, I focus on the transformations in gastrointestinal anatomy and function as the larvae undergo the broader metamorphic changes that prepare them to settle in the reef.
![Diagram of the common clownfish lifecycle between pelagic larval life and settlement into the reef](https://StefanoVianello.github.io/images/metamorphosis_Aocellaris.png)
<figcaption> Illustration of the lifecycle of the common clownfish. Larvae (rightmost) disperse into the ocean (pelagic phase). Major physiological, behavioral, and ecological changes (metamorphosis) take place as the larval body plan is recruited into the reef and the clownfish finds an anemome in which to house. Figure redrawn from (Roux et al. 2019)[https://doi.org/10.1002/dvdy.46]</figcaption>
![Microscope immunofluorescence larvae of clownfish, the day of hatching](https://StefanoVianello.github.io/images/Immunostaining_1dph.PNG)
<figcaption> Two larvae of the clownfish Amphiprion percula, collected on the day of hatching. Stains show the cell nuclei (light gray) and the epithelial cell junction component epithelial-cadherin (light blue)</figcaption>
![Fotographs of 3 clownfish larvae on the day of hatching (fixed)](https://StefanoVianello.github.io/images/Larvae_1dph.PNG)
<figcaption> Photograph of Amphiprion ocellaris clownfish larvae as seen down the microscope, on the day of hatching. Larvae were fixed and orange pigment cells were stripped by acetone treatment. The larvae appear black and white as a result. </figcaption> -->

<!-- <video src="https://StefanoVianello.github.io/images/1dph_larvae.mp4" data-canonical-src="https://StefanoVianello.github.io/images/1dph_larvae.mp4" controls="controls" muted="muted" class="d-block rounded-bottom-2 width-fit" style="max-height:640px;">
<figcaption> Hatched clownfish larvae swimming around in a small dish of seawater </figcaption>  --> 

<!--
**PhD research** <br/>
📑 **Read more about my research in [my most recent preprint](https://www.biorxiv.org/content/10.1101/2020.06.07.138883v3) and in [my doctorate thesis](https://infoscience.epfl.ch/record/291467).** Or click [here](https://splasho.com/upgoer5/?i=FJ4tqTuyVTMcpaA0VTMyqlOxLKymVUEbLKDtLJ5coJSfVTWuLzyyplOupzHtM3Wiq2yhMlOcoaAcMTHtqTuynKVtoJ90nTIlYPO3nTIhVUEbMKxtLKWyVUA0nJkfVUMypaxtqzIlrFOfnKE0oTHfVUEbMKxtnTS2MFO0olOaolO0nUWiqJqbVUMypaxtLzyaVTAbLJ5aMKZhVSEbMKxtLKWyVUA0nJkfVT1cp3AcozptLFOfo3Dto2LtnJ1jo3W0LJ50VTWiMUxtpTSlqUZuVSEbMKxtq2yfoPOhMJIxVTRtp3EioJSwnPO0olOyLKDtMz9iMPjtqTuyrFO3nJkfVT5yMJDtLFO3LKxtqT8tLaWyLKEbMFjtLJ5xVUEbMKxtq2yfoPOhMJIxVT1uoaxto3EbMKVtnJ5mnJEyVUOupaEmVUEiVTSfoT93VUEbMJylVTWiMTyyplO0olO3o3WeVTWyp3DhVSqyVT5iqlOeoz93VUEbLKDtoJShrFOiMvO0nTImMFOcoKOipaEuoaDtLz9xrFOjLKW0plOupzHtLaIcoUDtMaWioFO0nTHtp2SgMFOzLJ1coUxto2LtLaIcoTEcozptLzkiL2gmYvOWVUA0qJE5VUqbLKDtqTucplOzLJ1coUxto2LtLaIcoTEcozptLzkiL2gmVTAuovOxolO3nTIhVUEbMKxtLKWyVTW5VUEbMJ1mMJk2MKZfVUqcqTuiqKDtLJ55VTuyoUNtMaWioFO0nTHto3I0p2yxMF4tITucplOenJ5xVT9zVUqipzftnTIfpUZtqKZtLzI0qTIlVUIhMTIlp3EuozDtq2uuqPO0nTImMFOvqJyfMTyhMlOvoT9wn3ZtoT9inlOfnJgyYPObo3ptqTuyrFOeoz93VUqbLKDtqT8tMT8fVTuiqlO0nTI5VUEuoTftq2y0nPOiozHtLJ5iqTuypvO0olOvqJyfMPOuoTjtqTuyVTWiMUxtpTSlqUZtq2HtozIyMPjtLJ5xVUqbLKDtL291oTDtnTS2MFOao25yVUqlo25aVUqbMJ4tqTucplOxo2ImVT5iqPO3o3WeVT91qP4=) for a summary of my research in more accessible terms. <br/> <br/>
In humans, mice, and other mammals key internal organs such as the gut, lungs, pancreas, liver, thyroid, thymus, and bladder (and many others!) all derive from the same embryonic tissue: the endoderm. The development of all of these structures thus depends on a same set of early cells, and on the developmental instructions provided to them by the embryo. To study what these instructions might be, I am currently investigating the modes of development that endoderm cells (and their progenitors) execute when they can *not* rely on them. That is, when they are made to self-organise *in vitro* in a dish in the lab. Even on their own, endoderm cells emerge with timings and patterns comparable to what happens when they are on the embryo, and eventually form patterned structures in many way similar to the embryonic gut tube. My research touches on topics of endoderm and epithelial identity, self-organisation, patterning, and fundamental mammalian developmental biology.

![Gastruloids immunostained for endoderm marker FoxA2 and posterior marker TBra](https://StefanoVianello.github.io/images/TBra_foxA2_banner.PNG)
<figcaption> Embryonic stem cells can be left to self-organise into structures called Gastruloids. These provide an <i>in vitro</i> model of embryonic development. Endoderm cells, marked here in cyan (FoxA2), form an elongated internal core. The posterior marker TBra (gold) marks the posterior of the aggregate. </figcaption>

![Gastruloids next to the tailbud of a mouse embryo. The same makers have been immunostained in both.](https://StefanoVianello.github.io/images/Gastruloids_and_tail.PNG)
<figcaption> Gastruloids have been found to express genes in a organised way, in many way similar (and in many ways different) from that of the real mouse embryo. In the image above, the same markers have been stained in the tail of a mouse embryo (big structure on the right) and in 7-days-old Gastruloids. Insight comes from the comparison between what seen in the embryo and what observed to happen in these self-organising *in vitro* systems. </figcaption>

![Plots showing alternative quantifications of the marker expression patterns in Gastruloids](https://StefanoVianello.github.io/images/Gastruloid_quantification.PNG)
<figcaption> The patterns of gene expression amongst Gastruloids are very robust and reproducible. We can image entire populations of Gastruloids and extract spatial information about where specific genes are expressed along the main axis. </figcaption> --> 
