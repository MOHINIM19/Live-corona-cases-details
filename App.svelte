<script>

  import Button from "./Button.svelte";

  let regionData = [];

  let re = {};

  async function getdata() {

    const data = await fetch(

      "https://api.apify.com/v2/key-value-stores/toDWvRj1JpTXiM8FF/records/LATEST?disableRedirect=true"

    );

    re = await data.json();

  }

  async function getdata1() {

    const data = await fetch(

      "https://api.apify.com/v2/key-value-stores/toDWvRj1JpTXiM8FF/records/LATEST?disableRedirect=true"

    );

    regionData = re.regionData;

  }

</script>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<marquee behavior="scroll" direction="left" onmouseover="this.stop();" onmouseout="this.start();"scrollamount="7"style="font-size:17px">

🛑 COVID-19 ALERT---&nbsp;WEAR MASKS &nbsp;|| SANITISE YOUR HANDS FREQUENTLY &nbsp;|| KEEP  SOCIAL DISTANCE &nbsp;|| WASH YOUR HANDS &nbsp;|| GET VACCINATED AS SOON AS POSSIBLE &nbsp;|| STAY HOME STAY SAFE &nbsp; ||---COVID-19 ALERT 🛑

</marquee>

<h1 style="font-family:Times New Roman;font-size:70px;padding: 17px;text-align:center"> INDIA TODAY</h1>

<div class="scroll-left">

<p>🔷 Helpline Number 📞 :+91-11-23978046  &nbsp; ||&nbsp; Toll Free : 1075 &nbsp; || &nbsp; Helpline Email ID ✉ : ncov2019@gov.in 🔷 </p>

</div>

<h4 style="  font-style:sans-serif;

    font-size:17px;">CLICK ON TOGGLE FOR COLOR CHANGE:-</h4>

<Button>

    ⚜Toggle⚜ 💡

</Button>

<body>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

  <div>

<br>

  <h2 style="font-family:Verdana Bold;font-size:40px;text-align:center ;"> 📊 LIVE INDIA COVID CASE STATUS 📈</h2>

<button1 on:click={getdata()}>  </button1>

<br> <br>

<div style= " margin: auto;

  width: 30%;

  border: 3px solid green;

  padding: 20px; border-radius:20px;  background: url(https://www.lung.org/getmedia/734b6b16-c411-4c9a-b9b9-da25f7b9848e/covidblue_e.jpg?width=830&height=350&ext=.jpg);"> 

<h4 style="text-align:center;font-size:22px;">TOTAL CASES :  {re.totalCases}</h4>

<h4 style="text-align:center;font-size:22px"> ACTIVE CASES :  {re.activeCases}</h4>

<h4 style="text-align:center;font-size:22px"> RECOVERY :  {re.recovered}</h4>

<h4 style="text-align:center;font-size:22px"> DEATHS :  {re.deaths}</h4>

<br>  <br>

</div>

</div>

</body>

<body>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<br> <br> 

<h1 style="font-family:Verdana Bold;font-size:40px;text-align:center;">🛑 TO KNOW COVID CASES STATE WISE 🛑</h1>

<button on:click={getdata1}> 👉 CLICK HERE 👈</button>

<div class="box">

{#each regionData as region}

<br> 

<div style= " margin: auto;

  width: 40%;

  border: 3px solid green;

  padding: 10px; border-radius:20px; background:url(https://media.istockphoto.com/photos/coronavirus-covid19-under-the-microscope-on-light-background-picture-id1217531023?k=6&m=1217531023&s=170667a&w=0&h=PFUwy9WB_93dmaHppEzYnmrDOSFokyzKMqp7kxhDSfI=);">

<h2 style =" font-size:30px;">REGION</h2> 

<p style="font-family:georgia,garamond,serif;font-size:40px;font-style:Arial Italic;text-align:center">{region.region}</p>

<p style="font-family:Verdana;text-align:center;font-size:22px">TOTAL INFECTED CASES :{region.totalInfected}</p>

<p style="font-family:Verdana;text-align:center;font-size:22px">NEW INFECTED CASES :{region.newInfected}</p>

<p style="font-family:Verdana;text-align:center;font-size:22px">TOTAL ACTIVE CASES :{region.activeCases}</p>

<p style="font-family:Verdana;text-align:center;font-size:22px">TOTAL RECOVERED :{region.recovered}</p>

<p style="font-family:Verdana;text-align:center;font-size:22px">DEATHS :{region.deceased}</p>

</div>

{/each}

</div>

</body>

<div>

<div style= " width: 45%;

  border: 4px solid #FF0000;

  padding: 15px; border-radius:30px

  ;justify-content:center;margin:auto;

  background:url(https://image.shutterstock.com/image-vector/group-people-wearing-protection-medical-260nw-1671880660.jpg)"> 

  

  <h5 style="font-background:yellow;font-family:Verdana Bold;font-size:20px;"> Click below to get more info about CoVID Facilities in States/Union Territories</h5>

<a>

<input style="padding: 5px;

    font-style: Verdana Bold;

    font-size: 20px; 

    display: flex;  

    justify-content: center;  

    margin:auto;

    display: block;

 border: 4px solid; border-radius:15px;color:blue" type="button"value="🏙️ CoVID Facilities in States 🏙️"onclick="window.open('https://www.mohfw.gov.in/pdf/StatewiseCovidHospitalslink19062020.pdf')">

  </a>

</div>

<br>

<div style= " width: 35%;

  border: 4px solid #9933CC;

  padding: 40px; border-radius:30px;justify-content:center;margin:auto;

 background:url(https://ysm-res.cloudinary.com/image/upload/ar_16:9,c_fill,dpr_3.0,f_auto,g_faces:auto,q_auto:eco,w_500/v1/yale-medicine/live-prod/ym_new/images/3655000d-7adc-4e0f-a0ab-ac5d5ce337fa_tcm990-383423.jpg)" >

<h5 style="font-background:yellow;font-family:Verdana Bold;font-size:25px;border-radius: 20px;display:flex;justify-content:center;margin:auto"> Click below to register for Co-WIN Vaccination </h5>

<a>

<br>

<input style="padding: 4px;

    font-style: Verdana Bold;

    font-size: 20px;

    display: flex;  

    justify-content: center;  

    margin:auto;

    

    border: 6px solid; border-radius: 15px;color:red" type="button"value="💉 Register for Vaccination"onclick="window.open('https://selfregistration.cowin.gov.in/')">

  </a>

</div>

<br>

<div style= " width: 29%;

  border: 4px solid orange;

  padding: 40px; border-radius:30px;justify-content:center;margin:auto;

   background:url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR9YKbKgNVp2s-ttTWoeoEfklsL4vBWiX8I0A&usqp=CAU)">

  

<h5 style="font-background:yellow;font-family:Verdana Bold;font-size:30px;border-radius: 20px;display:flex;justify-content:center;margin:auto"> click below for covid donation </h5>

<a>

<br>

<input style="padding: 4px;

    font-style: Verdana Bold;

    font-size: 20px;

    display: flex;  

    justify-content: center;  

    margin:auto;

    

    border: 5px solid; border-radius: 11px;color:purple" type="button"value="❤ DONATE NOW ❤"onclick="window.open('https://covid.giveindia.org/cashrelief/')">

  </a>

</div>

</div>

<h1> </h1>

<br> 

<br>

<marquee behavior="scroll"direction="left"onmouseover="this.stop();" onmouseout="this.start();" scrollamount="10"style="font-size:17px">

<img src="http://www.stjosephs.edu.in/upload/image_upload/24b8a8e8ff3f8b6e63e14ddd20808306.jpg"  width="300" height="300" style="border-radius: 10px;margin:24px">

 <img src="https://www.newdelhiairport.in/media/1350/corona-mobile.jpg?q=20210107-A"  width="300" height="300"style="border-radius: 20px;margin:24px">

 <img src="https://pbs.twimg.com/media/Eq7eJ9gUwAEBy8k.jpg" height="300"style="border-radius: 20px;margin:24px" >

 <img src="https://pbs.twimg.com/media/Ez_KYhNUYAYBs9B.jpg"  width="300" height="300"style="border-radius: 20px;margin:24px">

  <img src="http://www.stjosephs.edu.in/upload/image_upload/f5a33fa08dc19700f833ff376f854eca.jpg"  width="300" height="300"style="border-radius: 20px;margin:24px">

</marquee>

<h4 style=" font-size:20px;"> Follow US On:click on the Names BELOW:-</h4>

<form>

 

 <a>

<input style="padding: 5px;

    font-style: italic;

    font-size: 12px;

    border: 3px solid; border-radius: 9px;color:blue" type="button"value="mohan"onclick="window.open('https://www.instagram.com/mohan_17m/')"> </a>

     </form>

     

     

     

     

     

     

     

     

     

    <meta name="viewport" content="width=device-width, initial-scale=1.0"> 

  <style>

  body {

    background: url(https://imgscf.slidemembers.com/docs/1/1/320/covid-19_simple_slides_templates_319762.jpg)

      no-repeat;

    background-size: cover;

    transition: background-color 1s;

  }

  :global(body.dark-mode) {

    background-color: paleturquoise;

    color: black;

    transition: background-color 0.6s;

    transition-delay: 0.5s;

  }

  button {

    padding: 10px;

    font-style: bold;

    font-size: 22px;

    border: 3px solid;

    display: flex;

    justify-content: center;

    align-items: center;

    margin: auto;

    display: block;

    border-radius: 9px;

  }

  button:hover {

    background-color: lightgreen;

    transform: scale(1.2) perspective(1px);

  }

  .box {

    height: 600px;

    border: 4px solid red;

    margin: 95px;

    overflow-y: scroll;

    border-radius: 20px;

    background: url(https://images.thequint.com/thequint%2F2020-07%2F485f0f71-e206-49bf-8602-830c63461f66%2Fcovidcases__1_.gif?auto=format%2Ccompress&fmt=webp&format=webp&w=480&dpr=2.6);

  }

  h2 {

    display: flex;

    justify-content: center;

  }

  .scroll-left {

    height: 50px;

    overflow: hidden;

    position: relative;

    background: rgb(247, 52, 52);

    color: whitesmoke;

    border: 1px solid rgb(255, 173, 211);

  }

  .scroll-left p {

    position: absolute;

    width: 90%;

    height: 900%;

    margin: 0;

    line-height: 50px;

    text-align: center;

    transform: translateX(100%);

    animation: scroll-left 15s linear infinite;

  }

  @keyframes scroll-left {

    0% {

      transform: translateX(40%);

    }

    100% {

      transform: translateX(-40%);

    }

  }

</style>

