<template>
  <div id="app">
    <Header/>
    <Intro/>
    <Portfolio/>
	<Skills/>
	<Experiences/>
	<Educations/>
	<Hobbies/>
	<Footer/>
	<Scroll-top-button/>
  </div>
</template>

<script>
import Header from './components/Header';
import Intro from './components/Intro';
import Portfolio from './components/Portfolio';
import Skills from './components/Skills';
import Experiences from './components/Experiences';
import Educations from './components/Educations';
import Hobbies from './components/Hobbies';
import Footer from './components/Footer';
import ScrollTopButton from './components/subComponents/ScrollTopButton';
import store from './vuex/store';


export default {
  name: 'App',
  components: {
    Header,
    Intro,
	Portfolio,
	Skills,
	Experiences,
	Educations,
	Hobbies,
	Footer,
	ScrollTopButton
  },
  store
}

</script>

<style>

/* ---------------------------------
1. PRIMARY STYLES
--------------------------------- */

html{ font-size: 100%; height: 100%; overflow-x: hidden; margin: 0px;  padding: 0px; touch-action: manipulation; }


body{ font-size: 16px; font-family: 'Poppins', serif; width: 100%; height: 100%; margin: 0; font-weight: 400;
	-webkit-font-smoothing: antialiased; -moz-osx-font-smoothing: grayscale; word-wrap: break-word; 
	color: #333; }

h1, h2, h3, h4, h5, h6, p, a, ul, span, li, img, inpot, button{ margin: 0; padding: 0; }

h1,h2,h3,h4,h5,h6{ line-height: 1.5; font-weight: inherit; }

h1,h2,h3{ font-family: 'Poppins', cursive; }

p{ line-height: 1.6; font-size: 1.05em; font-weight: 400; color: #777; }

h1{ font-size: 4em; line-height: 1; }
h2{ font-size: 2.2em; line-height: 1.1; }
h3{ font-size: 1.8em; }
h4{ font-size: 1.3em; }
h5{ font-size: 1em; }
h6{ font-size: .9em; letter-spacing: 1px; }

a, button{ display: inline-block; text-decoration: none; color: inherit; line-height: 1; 
	-webkit-transition: all .25s ease-in-out; transition: all .25s ease-in-out; }

a:focus, a:active, a:hover,
button:focus, button:active, button:hover,
a b.light-color:hover{ text-decoration: none; color: #023859; }

b{ font-weight: 600; }

img{ width: 100%; }

li{ list-style: none; display: inline-block; }

span{ display: inline-block; }

button{ outline: 0; border: 0; background: none; cursor: pointer; }

.icon{ font-size: 1.1em; display: inline-block; line-height: inherit; }

[class^="icon-"]:before, [class*=" icon-"]:before{ line-height: inherit; }

b.max-bold{ font-weight: 700; }


/* ---------------------------------
2. COMMONS FOR PAGE DESIGN
--------------------------------- */

.section{ padding: 100px 0 50px; }

.section .heading{ margin-bottom: 60px; }

.section .heading:before{ content:''; height: 10px; width: 50px; border-radius: 5px;
	margin-bottom: 20px; display: block; background: #0f5a8c; }
	
.margin-t-10{ margin-top: 10px; }

.margin-b-30{ margin-bottom: 30px; }
.margin-b-50{ margin-bottom: 50px; }

.margin-tb-30{ margin-top: 30px; margin-bottom: 30px; }

.font-blue{ color: #3782aa; }

.font-semi-white{ color: #ddd; }

.font-lite-black{ color: #999; }



/* ---------------------------------
RESPONSIVE
--------------------------------- */



/* Screens Resolution : 992px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 1200px) {
	/* ---------------------------------
	9. COUNTER SECTION
	--------------------------------- */

	.counter-section{ text-align: center; padding: 50px 0 20px; }

	.counter{ display: inline-block; }
	
	.counter .desc{ text-align: left; }
}

/* Screens Resolution : 992px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 992px) {
	
	/* ---------------------------------
	4. INTRO SECTION
	--------------------------------- */

	.intro-section{ padding-top: 250px; }
	
}

/* Screens Resolution : 767px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 767px) {
	
	/* ---------------------------------
	1. PRIMARY STYLES
	--------------------------------- */

	p{ line-height: 1.4; }

	h1{ font-size: 3em; }
	h2{ font-size: 2em; }
	h3{ font-size: 1.8em; }


	
	/* ---------------------------------
	2. COMMONS FOR PAGE DESIGN
	--------------------------------- */

	.section{ padding: 50px 0 0px; }

	.section .heading{ margin-bottom: 30px; }

	
	/* ---------------------------------
	4. INTRO SECTION
	--------------------------------- */

	.intro-section{ padding-top: 350px; }


	/* ---------------------------------
	5. PORFOLIO SECTION
	--------------------------------- */

	.portfolio-section{ padding-bottom: 0; }
	
	.portfolio-section .portfolioFilter{ margin: 0px 0 10px; }
	
	.portfolio-section .portfolioContainer{ margin-left: 0; margin-right: 0; }

	.portfolio-section .p-item{ width: 50%; padding: 0 15px 0px; }

	.portfolio-section .p-item{ max-width: 400px; }

	
	/* ---------------------------------
	8. EDUCATION SECTION
	--------------------------------- */
	
	.education-wrapper:after,
	.education-wrapper .education:after{ display: none; }

}

/* Screens Resolution : 575px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 575px) {
	
	/* ---------------------------------
	1. PRIMARY STYLES
	--------------------------------- */

	body{ font-size: 14px;  }
	

	/* ---------------------------------
	5. PORFOLIO SECTION
	--------------------------------- */
	
	.portfolio-section .p-item{ width: 100%; }
	
}

/* Screens Resolution : 479px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 479px) {


}

/* Screens Resolution : 359px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 359px) {
	
	/* ---------------------------------
	3. HEADER
	--------------------------------- */

	header .heading-wrapper{  padding: 30px 20px 20px; }

	header .info .icon{ font-size: 25px; }

	header .info .right-area{ margin-left: 35px; }

}

/* Screens Resolution : 290px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 290px) {

	
}

/* Screens Resolution : 290px
-------------------------------------------------------------------------- */
@media only screen and (max-width: 260px) {
	
	/* ---------------------------------
	3. HEADER
	--------------------------------- */

	header .heading-wrapper{  padding: 10px 15px 0px; }

	header .info .icon{ font-size: 15px; }

	header .info .right-area{ margin-left: 20px; }
	
	/* ---------------------------------
	4. INTRO SECTION
	--------------------------------- */

	.intro .profile-img{ width: 80%; height: auto; top: 0; margin-bottom: 10px; }
	
	.intro{ padding: 20px 10px 0; margin-right: -15px; margin-left: -15px; }
	
}

</style>
