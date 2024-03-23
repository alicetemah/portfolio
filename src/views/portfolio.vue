<script  lang="ts" setup>
import {ref} from 'vue';


const __name="Portfolio"
const name = ref("Alice Busiah ")
const role = ref("Full-Stack Developer")
const email=ref("alicecodinglab@gmail.com")
const website=ref("https://alicetemah.github.io/")
const education=ref([{degree:"Abitur",school:'Gymnasium Nepomucenum',date:"2008-2016", link:undefined},{degree:"Bachelor of Science Information Systems",school:'Universtät zu Köln', date:"2016-2022", link:undefined},{degree:"Nanodegree Self-Driving Car", school:"UDACITY inc. Mountain View California", date:"2021", link:'https://www.udacity.com/certificate/UA7TJJTT'},{
  degree:"Master of Science Applied Computer Science", school:"Ruhr Universität Bochum", date:"2022-today", link:undefined}])
const portfolio= ref([
  {name:"Table Tea Frontend",type:"Frontend",link:'https://tabletea.netlify.app/', description:"A Frontend Application for a Fullstack App that allows users to create,upload or select tables and automatically create different types of charts with just a few clicks", stack:['Vue.js','Nuxt', 'Tailwindcss', 
  'Daisyui','CSS', 'HTML'], deployment:"Netlify"},{name:"Table Tea Backend",type:"Backend",link:'https://tabletea.netlify.app/login',"description":"A Backend Application that acts as a REST API and serves data from a databse as requested from the client given that the client posseses adequate authentication and authorization", stack:['Express.js','MongoDB'] }, {name:'Portfolio',link:'https://alicetemah.github.io/', type:'Frontend',description:'A single page application that summarizes my profile as a Developer',stack:['Vue.js', 'CSS'], deployment:'Github'}
])
const skills =[{type:'Frontend',stack:['JavaScript', 'Typescript','Vue.js', 'Nuxt','HTML','CSS','Tailwindcss']}, {type:'Backend',stack:['Express.js','MongoDB']}, {type:'Version Control', stack:['Git', 'Github']}]

const navigateTo=(link)=>{
  
  window.location.href = link


}
education.value = education.value.reverse()

</script>
<style>
  @font-face {
    font-family: 'Archivo Black';
    src: url('/ArchivoBlack-Regular.ttf') format('truetype');

  }


  @font-face {
    font-family: 'Bridger';
    src: url('/Bridger.otf') format('opentype');

  }


  h1{
    font-family: 'Archivo Black','sans-serif';
  }


  b {
    font-weight:100;
  }



  .pageTitle{
    font-family: 'Bridger'; 
    font-size: 5vh; 
    font-weight: 1000;
    padding-right: 2rem;
  

  }
  .sectionTitle{

    margin-top: 3rem;

  }

  svg {
    display: inline;
    width: 1rem;
    height: auto;
  }


  .mainBox{
    display: flex;
    flex-direction: column;
    width: 50rem;
    height: auto;
    padding: 10rem;
  }

  .mysection{
    display: grid;
    grid-template-columns: 20rem 20rem;
    column-gap: 2rem;
    row-gap: 2rem;
    
    margin-top:3rem;

  }


  .mycircle{
    display: flex;
    width:100%;
    height: auto;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-radius: 3rem;
    border: 2px solid;
    font:bold;

  }

  .myrec{
    display: flex;
    flex-direction: column;
    width:100%;
    height: auto;
    border: 1px solid;
    border-radius: 0.25rem;
    padding: 1rem;
  }

  button{
    border-radius: 1rem;
  }
  button:hover{
    background-color: rgb(102, 130, 106);
    color: white;
  }

  .head {
    display: grid;
    grid-template-columns: 1fr 1fr;
    width: 50vh;
    height:auto;
    margin-bottom: 2rem;
    margin-top: 0rem;
  }

  img {
    height: 20vh;
    width: auto;
  }
  .profilepic{
    place-self: center;
    height:auto;
    width: auto;
    background-size: cover;

  }

</style>
<template>
<div class="mainBox">

  <div class="head">
    <div>
      <h1 class="pageTitle">RESUME</h1>
      <h1 class="pageTitle">{{ role }}</h1>
    </div>         
    <div class="profilepic">
      <img height="100%
      " width="auto" src="/profilepic.png"/>
    </div>
    <div>       
        <h1 class="pageTitle">{{ name }}</h1>
    </div>
    <div class="myrec">       
          <div>
            <div class="svgIcon"><svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="122.879px" height="88.855px" viewBox="0 0 122.879 88.855" enable-background="new 0 0 122.879 88.855" xml:space="preserve"><path d="M7.048,0h108.784c1.939,0,3.701,0.794,4.977,2.069c1.277,1.277,2.07,3.042,2.07,4.979v74.759 c0,1.461-0.451,2.822-1.221,3.951c-0.141,0.365-0.361,0.705-0.662,0.994c-0.201,0.189-0.422,0.344-0.656,0.461 c-1.225,1.021-2.799,1.643-4.508,1.643H7.048c-1.937,0-3.701-0.793-4.979-2.07C0.794,85.51,0,83.748,0,81.807V7.048 c0-1.941,0.792-3.704,2.068-4.979C3.344,0.792,5.107,0,7.048,0L7.048,0z M5.406,78.842l38.124-38.22L5.406,9.538V78.842 L5.406,78.842z M47.729,44.045L8.424,83.449h105.701L76.563,44.051L64.18,54.602l0,0c-0.971,0.83-2.425,0.877-3.453,0.043 L47.729,44.045L47.729,44.045z M80.674,40.549l36.799,38.598V9.198L80.674,40.549L80.674,40.549z M8.867,5.406l53.521,43.639 l51.223-43.639H8.867L8.867,5.406z"/></svg></div>
            <p>{{ email }}</p> 
          </div> 
          <div>
            <div class="svgIcon"><svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="122.879px" height="122.879px" viewBox="0 0 122.879 122.879" enable-background="new 0 0 122.879 122.879" xml:space="preserve"><path d="M109.465,89.503c0.182,0,0.359,0.019,0.533,0.053c1.146-1.998,2.191-4.095,3.135-6.286 c0.018-0.044,0.037-0.086,0.059-0.128c1.418-3.345,2.488-6.819,3.209-10.419c0.559-2.793,0.904-5.657,1.035-8.591h-16.893 c-0.307,8.574-2.867,17.03-7.639,25.371H109.465L109.465,89.503z M106.52,94.889H89.506c-5.164,7.481-12.121,14.87-20.838,22.167 c1.367-0.17,2.719-0.388,4.055-0.655c3.646-0.729,7.164-1.817,10.549-3.264l-0.002-0.004c3.441-1.48,6.646-3.212,9.609-5.199 c2.969-1.992,5.721-4.255,8.25-6.795l0.01-0.01l0,0C103.096,99.18,104.889,97.099,106.52,94.889L106.52,94.889z M54.21,117.055 c-8.716-7.296-15.673-14.685-20.838-22.166H16.361c1.631,2.21,3.423,4.291,5.379,6.24l0.01,0.011v-0.001 c2.53,2.54,5.282,4.803,8.25,6.795c2.962,1.987,6.167,3.719,9.609,5.199c0.043,0.019,0.086,0.038,0.128,0.059 c3.345,1.419,6.819,2.488,10.42,3.209C51.493,116.668,52.843,116.886,54.21,117.055L54.21,117.055z M12.852,89.503h17.122 c-4.771-8.341-7.332-16.797-7.637-25.371H5.445c0.13,2.934,0.475,5.797,1.034,8.59c0.729,3.646,1.818,7.164,3.264,10.549 l0.004-0.001C10.682,85.442,11.716,87.521,12.852,89.503L12.852,89.503z M5.445,58.747h16.997c0.625-8.4,3.412-16.857,8.407-25.371 H12.852c-1.136,1.982-2.17,4.061-3.105,6.234c-0.019,0.043-0.039,0.086-0.059,0.127C8.269,43.083,7.2,46.557,6.479,50.157 C5.92,52.95,5.575,55.814,5.445,58.747L5.445,58.747z M16.361,27.991h17.938c5.108-7.361,11.862-14.765,20.29-22.212 c-1.496,0.175-2.973,0.408-4.431,0.7c-3.647,0.729-7.164,1.818-10.549,3.264l0.001,0.003c-3.442,1.481-6.647,3.212-9.609,5.2 c-2.968,1.992-5.72,4.255-8.25,6.794l-0.011,0.01h0C19.784,23.7,17.992,25.78,16.361,27.991L16.361,27.991z M68.289,5.778 c8.428,7.447,15.182,14.851,20.291,22.212h17.939c-1.631-2.21-3.424-4.291-5.381-6.24l-0.01-0.01l0,0 c-2.529-2.54-5.281-4.802-8.25-6.794c-2.963-1.988-6.168-3.719-9.609-5.2c-0.043-0.018-0.086-0.038-0.127-0.059 c-3.346-1.418-6.82-2.488-10.42-3.208C71.264,6.187,69.785,5.954,68.289,5.778L68.289,5.778z M110.027,33.376H92.029 c4.996,8.514,7.783,16.971,8.408,25.371h16.998c-0.131-2.934-0.477-5.797-1.035-8.59c-0.73-3.646-1.818-7.164-3.264-10.549 l-0.004,0.002C112.197,37.437,111.164,35.358,110.027,33.376L110.027,33.376z M49.106,1.198C53.098,0.399,57.21,0,61.44,0 c4.23,0,8.341,0.399,12.333,1.198c3.934,0.788,7.758,1.97,11.473,3.547c0.051,0.018,0.1,0.037,0.148,0.058 c3.703,1.594,7.197,3.485,10.471,5.684c3.268,2.192,6.291,4.677,9.066,7.462c2.785,2.775,5.27,5.799,7.461,9.065 c2.197,3.275,4.09,6.768,5.684,10.473l-0.004,0.001l0.004,0.009c1.607,3.758,2.809,7.628,3.605,11.609 c0.799,3.992,1.197,8.104,1.197,12.334c0,4.23-0.398,8.343-1.197,12.335c-0.787,3.932-1.971,7.758-3.547,11.472 c-0.018,0.05-0.037,0.099-0.059,0.147c-1.594,3.705-3.486,7.197-5.684,10.472c-2.191,3.267-4.676,6.29-7.461,9.065 c-2.775,2.785-5.799,5.271-9.066,7.462c-3.273,2.198-6.768,4.091-10.471,5.684l-0.002-0.004l-0.01,0.004 c-3.758,1.606-7.629,2.808-11.609,3.604c-3.992,0.799-8.104,1.198-12.333,1.198c-4.229,0-8.342-0.399-12.334-1.198 c-3.933-0.787-7.758-1.97-11.474-3.546c-0.049-0.019-0.098-0.037-0.147-0.059c-3.705-1.593-7.197-3.485-10.472-5.684 c-3.266-2.191-6.29-4.677-9.065-7.462c-2.785-2.775-5.27-5.799-7.461-9.065c-2.198-3.274-4.09-6.767-5.684-10.472l0.004-0.002 l-0.004-0.009c-1.606-3.758-2.808-7.628-3.604-11.609C0.4,69.782,0,65.67,0,61.439c0-4.229,0.4-8.342,1.199-12.334 c0.787-3.933,1.97-7.758,3.546-11.473c0.018-0.049,0.037-0.099,0.058-0.147c1.594-3.705,3.485-7.198,5.684-10.473 c2.192-3.266,4.677-6.29,7.461-9.065c2.775-2.785,5.799-5.27,9.065-7.462c3.275-2.198,6.768-4.09,10.472-5.684l0.001,0.004 l0.009-0.004C41.254,3.197,45.125,1.995,49.106,1.198L49.106,1.198z M64.133,9.268v18.723h17.826 C77.275,21.815,71.34,15.575,64.133,9.268L64.133,9.268z M64.133,33.376v25.371h30.922c-0.699-8.332-3.789-16.788-9.318-25.371 H64.133L64.133,33.376z M64.133,64.132v25.371h22.51c5.328-8.396,8.189-16.854,8.531-25.371H64.133L64.133,64.132z M64.133,94.889 v18.952c7.645-6.283,13.902-12.601,18.746-18.952H64.133L64.133,94.889z M58.747,113.843V94.889H40 C44.843,101.24,51.1,107.559,58.747,113.843L58.747,113.843z M58.747,89.503V64.132H27.706c0.341,8.518,3.201,16.975,8.531,25.371 H58.747L58.747,89.503z M58.747,58.747V33.376H37.143c-5.529,8.583-8.619,17.04-9.319,25.371H58.747L58.747,58.747z M58.747,27.991 V9.266C51.54,15.573,45.604,21.815,40.92,27.991H58.747L58.747,27.991z"/></svg></div>
            <p>{{ website}}</p>
          </div>                      
    </div>    
  </div>
  
  <div class="mysection">

  </div>


  <h1 class="sectionTitle">EDUCATION</h1>
    <div class="mysection">
      <div v-for="edu in education">
        <div class="mycircle"><p><b>{{edu.date}}</b></p></div>
        <div class="myrec"><p>{{ edu.degree }}</p></div>
        <div class="myrec"><p>@{{ edu.school }}</p><button v-if="edu.link" @click="()=>navigateTo(edu.link)">Link to Certificate</button></div>
      </div>
  </div>

 
  <h1 class="sectionTitle">EXPERIENCE</h1>
  <div class="mysection">
    <div v-for="project in portfolio">
      <div class="mycircle"><p>{{project.type}}</p></div>
      <div class="myrec">
        <p><b>{{ project.name }}</b></p>        
        <p>{{ project.description }}</p>
        <button v-if="project.link" @click="()=>navigateTo(project.link)">Link to Project</button>
      </div>
      <div class="myrec">        
          <ul>
            <li v-for="app in project.stack">{{app}}</li>
          </ul>        
      </div>
    </div>
  </div>

  
  <h1 class="sectionTitle">SKILLS</h1>
  <div class="mysection">
      <div v-for="skill in skills">
          <div class="mycircle"><p>{{skill.type}}</p></div>
          <div class="myrec">
            <ul>
              <li v-for="app in skill.stack"> {{ app }}</li>
            </ul>
          </div>
      </div>
    </div>

</div>

</template>
