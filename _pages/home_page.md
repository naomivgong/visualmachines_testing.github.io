---
title: " "
layout: home
sitemap: false
permalink: /
header:
  overlay_image: /assets/images/vmgHomeMain.png

# excerpt: >
#   <h4>Giving Robots the Gift of Sight</h4><h5>Superhuman cameras enable superhuman robotics,<br>advancing cyberphysical systems and digital health</h5>
head_scripts:

---
 

<main role="main" class="container-fluid">
  <div class="row slideshow">

  <div class="dots-container">
      {% for slide in site.data.slides %}
        <span class="dot" onclick="currentSlide({{ forloop.index0 }})"></span>
      {% endfor %}
    </div>
    {% for slide in site.data.slides %}
    <div class="col-md-12 image-wrapper slide">
      <img src="{{site.baseurl}}/assets/images/coverpages/{{ slide.image_link }}" class="img-fluid" style="max-width: 100%;">
      <div class="over-text d-none d-md-none d-lg-block">
        <div class="heading" style="color:#302b2b;">{{ slide.title }}</div>
        <div class="body-home" style="color:white;">
          {{ slide.description }}
          <br>
          <a href="{{ slide.article_link }}" class="btn btn-primary">Read More</a>
        </div>
      </div>
    </div>
    {% endfor %}
  </div>
</main>





<style>

.btn {
    color: #8f3985; 
    background-color: white; 
    border: 1px solid #8f3985; 
    padding: 10px 20px; 
    text-decoration: none; 
    display: inline-block; 
    border-radius: 4px; 
    transition: background-color 0.3s, color 0.3s; 
}

.btn:hover {
    background-color: #8f3985; /* Darker background color on hover */
    color: white; /* Text color becomes white on hover */
}



  /* CSS for slideshow */
.slideshow {
  position: relative;
  height: 400px;
}

.slide {
  position: absolute;
  left: 0;
  top: 0;
  opacity: 0;
  visibility: hidden; /* Hide non-active slides */
  transition: opacity 1s ease-in-out, visibility 0.5s ease-in-out; /* Smooth opacity and visibility transition */
  width: 100%;
  margin: 0;
  padding: 0;
}

.slide.active {
  opacity: 1; 
  visibility: visible; 
}


.over-text {
  position: absolute;
  top: calc(50% - 40px); /* Adjust this value as needed to align with dots */
  left: 100px; 
  color: #8f3985;
  padding: 20px;
  max-width: 600px;
  border-radius: 5px;
  transform: translateY(-50%); 
  opacity: 1;
  text-align: center; /* Center the text horizontally */
}
.heading {
  font-size: 30px;
  font-weight: bold;
  margin-bottom: 10px;
}
.body-home {
  font-size: 16px;
}

.img-fluid {
  margin: 0 auto; /* Center the image horizontally */
}


  .dots-container {
    position: absolute;
    top: 50%; /* Center vertically */
    left: 10px; /* Adjust left position as needed */
    transform: translate(-50%, -50%);
    z-index: 1000;
  }


.dot {
  height: 8px;
  width: 8px;
  margin: 4px 0; 
  background-color: #bbb;
  border-radius: 50%;
  display: block;
  transition: background-color 0.6s ease;
  cursor: pointer;
}

.dot.active {
  background-color: #717171;
}

.dot:hover {
  background-color: #717171;
}

/* Fading animation for slides */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

</style>



<script>
  document.addEventListener("DOMContentLoaded", function() {
  const slides = document.querySelectorAll('.slide');
  const dots = document.querySelectorAll('.dot');
  let currentSlide = 0;
  const slideInterval = 5000; // Interval in milliseconds (3 seconds)

  function showSlide(index) {
    slides[currentSlide].classList.remove('active');
    dots[currentSlide].classList.remove('active');
    currentSlide = index;
    slides[currentSlide].classList.add('active');
    dots[currentSlide].classList.add('active');
  }

  function nextSlide() {
    showSlide((currentSlide + 1) % slides.length);
  }

  // Show the first slide initially
  showSlide(currentSlide);

  // Automatically move to the next slide every slideInterval milliseconds
  const intervalId = setInterval(nextSlide, slideInterval);

  // Add click event listeners to dots
  dots.forEach((dot, index) => {
    dot.addEventListener('click', function() {
      clearInterval(intervalId); // Stop the automatic slideshow
      showSlide(index);
      setTimeout(function() { // Restart the automatic slideshow after a click
        setInterval(nextSlide, slideInterval);
      }, slideInterval);
    });
  });
});




</script>







<br>



<main role="main" class="container">
  <div class="row">
    <div class="col-md-5 offset-md-1">
      <div class="heading-home" style="color:#8f3985; margin-top: 120px;">News</div>





      
 <div class="heading-home padded-top">Aug 2023: Diffusion w/ Perspective appears in SIGGRAPH Asia</div>
        <div class="body-home">Rishi's first author paper appears in the journal proceedings of SIGGRAPH Asia</div>

                <div class="heading-home padded-top">Apr 2023: Six papers accepted</div>
        <div class="body-home">Four papers in CVPR 2023, One in Nature Mach. Intell., One in IEEE Access.</div>
        
	    <div class="heading-home padded-top">Dec 2022: Achuta wins IEEE-HKN Under 35 Award</div>
	    <div class="body-home">For inclusive inventions in EECS and bioengineering. <a style="color: purple;" href="https://www.ee.ucla.edu/prof-kadambi-wins-ieee-hkn-under-35-award/">UCLA Article.</a></div>
     
             <div class="heading-home padded-top">Nov 2022: Pradyumna and Achuta win UIST Best Demo Award (Hon. Mention)</div>
        <div class="body-home">A pressure-sensitive speckle sensor to enable humans to interact with ordinary surfaces as if they were touch sensors.</div>   
        
                     <div class="heading-home padded-top">April 2022: Ellin wins NSF GRFP PhD Fellowship</div>
        <div class="body-home">For proposed research on making mHealth devices work in an inclusive manner. <a style="color: purple;" href="https://samueli.ucla.edu/ucla-engineering-students-receive-2022-nsf-graduate-research-fellowships/">UCLA Newsroom.</a></div>   

             
        <div class="heading-home padded-top">Feb 2022: MIT Press Textbook is in Print</div>
        <div class="body-home">Computational Imaging available for purchase or as <a style="color: purple;" href="http://imagingtext.github.io/">free download</a>.</div>
           
        
        <div class="heading-home padded-top">Sep 2021: Achuta wins DARPA YFA</div>
	    <div class="body-home">Details in the <a style="color: purple;" href="https://samueli.ucla.edu/ucla-electrical-engineer-receives-darpa-young-faculty-award-for-contactless-covid-testing/">UCLA Newsroom</a>.</div>
     
     
        <div class="heading-home padded-top">May 2021: Achuta wins ARO YIP Award</div>
	    <div class="body-home">Details in the <a style="color: purple;" href="https://samueli.ucla.edu/ucla-professor-awarded-us-army-young-investigator-grant-for-fairness-in-ai-research/">UCLA Newsroom</a>.</div>  
	    
        <div class="heading-home padded-top">April 2021: Medical device paper in Science</div>
      <div class="body-home">On the fairness of medical device physics.</div>
	 
        <div class="heading-home padded-top">March 2021: Achuta wins NSF CAREER Award</div>
	    <div class="body-home">Details on the <a style="color: purple;" href="https://www.nsf.gov/awardsearch/showAward?AWD_ID=2046737&HistoricalAwards=false">NSF Website</a>. </div> 

      <br>
    </div>
    <div class="col-md-5 offset-md-1">
      <div class="heading-home" style="color:#8f3985; margin-top: 120px;">Current Teaching</div>
      <div class="heading-home padded-top">Winter 2024</div>
      <div class="body-home">ECE 149: Foundations of Computer Vision</div>
      <div class="heading-home padded-top">Fall 2023</div>
      <div class="body-home">ECE 239AS: Computational Imaging</div>
      <div class="heading-home padded-top">Fall 2022</div>
      <div class="body-home">ECE 113: Discrete-Time Signal Processing</div>
      <div class="heading-home padded-top">Winter 2023</div>
      <div class="body-home">ECE 113: Discrete-Time Signal Processing</div>
      <div class="heading-home padded-top">Spring 2023</div>
      <div class="body-home">ECE 188 / CS 188: Introduction to Computer Vision</div>
      <div class="heading-home padded-top">Achuta Office Hours (2023)</div>
      <div class="body-home">Wed. 10-11am in E4, 56-147J</div>
      <!--<div class="heading-home padded-top">Winter 2019</div>-->
      <!--<div class="body-home">EE 211: Digital Image Processing</div>-->
      <!--<div class="heading-home padded-top">Spring 2019</div>-->
      <!--<div class="body-home">TBD</div>-->
      <br>
    </div>
  </div>
</main> <!-- container -->