<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio</title>
    <style>
        *{
    margin: 0;
    padding: 0;
    font-family:'Poppins',sans-serif;
    box-sizing: border-box;
    }
    body{
        background: black;
        color: #fff;
    }
    #header{
        width: 100%;
        height: 100vh;
        background-image:url(background.webp) ;
        background-size: cover;
        background-position: center;
    }
    .container{
        padding:10px 3%;
    }
    .logo{
        width: 50px;
        height: 50px;
    }
    nav{
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
    }
    nav ul li{
        display: inline-block;
        list-style: none;
        margin: 10px 20px;
    }
    nav ul li a{
        color: #fff;
        text-decoration: none;
        font-size: 18px;
        position: relative;
    }
    nav ul li a::after{
        content: '';
        width: 0;
        height: 3px;
        background: #ff004f;
        position: absolute;
        left: 0;
        bottom: -6px;
        transition: 0.5s;
    }
    nav ul li a:hover::after{
        width: 100%;
    }
    .header-text{
        margin-top: 20%;
        font-size: 30px;
    }
    .header-text h1{
        font-size: 60px;
    }
    .header-text h1 span{
        color:#ff004f;
    }
    /*------------about-----------*/
    #about{
        padding: 80px 0;
        color:#ababab;
    }
    .row{
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
    }
    .about-col-1{
        flex-basis: 35%;
    }
    .about-col-1 img{
        width: 100%;
        border-radius: 15px;
    }
    .about-col-2{
        flex-basis: 55%;
    }
    .sub-title{
        font-size: 60px;
        color: white;
    }
    .tab-titles{
        display: flex;
        margin: 20px 0 40px;
    }
    .tab-links{
        margin-right: 50px;
        font-size: 18px;
        font-weight: 500;
        cursor: pointer;
        position: relative;
    }
    .tab-links::after{
        content: '';
        width: 0;
        height: 3px;
        background: #ff004f;
        position: absolute;
        left: 0;
        bottom: -6px;
        transition: 0.5s;
    }
    .tab-links.active-link::after{
        width: 50%;
    }
    .tab-contents ul li{
        list-style: none;
        margin: 10px 0;
    }
    .tab-contents ul li span{
        color: #ff004f;
        font-size: 14px;
    }
    .tab-contents{
        display: none;
    }
    .tab-contents.active-tab{
        display: block;
    }
    /*---------------------services--------------------*/
    #services{
        padding: 30px 0;
    }
    .services-list{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        grid-gap: 40px;
        margin-top: 50px;
    }
    .services-list div{
        background: #262626;
        padding: 40px;
        font-size: 13px;
        font-weight: 300;
        border-right: 10px;
        border-radius: 10px;
        transition: background 0.5s, transform 0.5s;
    }
    .services-list div i{
        font-size: 30px;
        margin-bottom: 30px;
    }
    .services-list div h2{
        font-size: 30px;
        font-weight: 500;
        margin-bottom: 15px;
    }
    .services-list div a{
        text-decoration: none;
        color: #fff;
        font-size: 12px;
        margin-top: 20px;
        display: inline-block;
    }
    .services-list div:hover{
        background: #ff004f;
        transform: translateY(-10px);
    }
    /*-----------portfolio-------*/
    #portfolio{
        padding: 50px 0;
    }
    .work-list{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        grid-gap: 40px;
        margin-top: 50px;
    }
    .work{
        border-radius: 10px;
        position: relative;
        overflow: hidden;
    }
    .work img{
        width: 100%;
        border-radius: 10px;
        display: block;
        transition: transform 0.5s;
    }
    .layer{
        width: 100%;
        height: 0;
        background: linear-gradient(rgba(0,0,0,0.6),#ff004f);
        border-radius: 10px;
        position: absolute;
        left: 0;
        bottom: 0;
        overflow: hidden;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        padding: 0 40px;
        text-align: center;
        font-size: 14px;
        transition: height 0.5s;
    }
    .layer h3{
        font-weight: 500;
        margin-bottom: 20px;
    }
    .layer a{
        margin-top: 20px;
        color: #ff004f;
        text-decoration: none;
        font-size: 18px;
        line-height: 60px;
        background: #fff;
        width: 60px;
        height: 60px;
        border-radius: 50%;
        text-align: center;
    }
    .work:hover img{
        transform: scale(1.1);
    }
    .work:hover .layer{
        height: 100%;
    }
    .btn{
        display: block;
        margin: 50px auto;
        width: fit-content;
        border: 1px solid #ff004f;
        padding: 14px 50px;
        border-radius: 6px;
        text-decoration: none;
        color: #fff;
        transform-origin: background 0.5s;
    }
    .btn:hover{
        background: #ff004f;
    }
    /* ----------------contact----------------- */
    .contact-left{
        flex-basis: 35%;
    }
    .contact-right{
        flex-basis: 60%;
    }
    .contact-left p{
        margin-top: 15px;
    }
    .contact-left p i{
        /* color: #ff004f; */
        margin-right:  15px;
        font-size: 25px;
    }
    .social-icons a{
        margin-top: 20px;
        text-decoration: none;
        font-size: 28px;
        margin-right: 15px;
        color: #ababab;
        display: inline-block;
        transition: transform 0.3s;
    }
    .social-icons a:hover{
        color: #ff004f;
        transform: translateY(-5px);
    }
    .btn.btn2{
        margin-top: 20px;
        display: inline-block;
        background: #ff004f;
    }
    .contact-right form{
        width: 100%;
    }
    form input, form textarea{
        width: 100%;
        border: 0;
        outline: none;
        background: #262626;
        padding: 15px;
        margin: 15px 0;
        color: #fff;
        font-size: 18px;
        border-radius: 6px;
    }
    form .btn2{
        padding: 14px 60px;
        margin-top: 20px;
        cursor: pointer;
        font-size: 18px;
    }
    .copyright{
        width: 100%;
        text-align: center;
        padding: 25px 0;
        background: #262626;
        font-weight: 300;
        margin-top: 20px;
    }
    .copyright i {
        color: #ff004f;
    }
    nav .fas{
            display: none;
            font-size: 25px;
        }
        
    /*--------------------css for small screens-----------*/
    

    @media only screen and (max-width:600px){
        #header{
            background-image: url(background2.webp);
        }
        .header-text{
            margin-top: 95%;
            font-size: 16px;
        }
        .header-text h1{
            font-size: 30px;
        }
        nav .fas{
            display: block;
            font-size: 25px;
        }
        nav ul{
            background: #ff004f;
            position: fixed;
            top: 0;
            right: -200px;
            width: 200px;
            height: 100vh;
            padding-top: 50px;
            z-index: 2;
            transition: right 0.5s;
        }
        nav ul li{
            display: block;
            margin: 25px;
        }
        nav ul .fas{
            position: absolute;
            top: 25px;
            left: 25px;
            cursor: pointer;
        }
        .sub-title{
            font: size 40px;
        }
        .about-col-1,.about-col-2{
            flex-basis:100%;
        }
        .about-col-1{
            margin-bottom: 30px;
        }
        .about-col-2{
            font-size: 14px;
        }
        .tab-links{
            font-size: 16px;
            margin-right: 20px;
        }
        .contact-left,.contact-right{
            flex-basis: 100%;
        }
        .copyright{
            font-size: 14px;
        }
    }
    </style>
    <script src="https://kit.fontawesome.com/dd847e2b63.js" crossorigin="anonymous"></script>
</head>
<body>
   <div id="header">
        <div class="container">
            <nav>
                <img src="1.webp" class="logo" href="page.html"> 
                <ul id="sidemenu">
                    <li><a href="page.html">Home</a></li>
                    <li><a href="#About">About</a></li>
                    <li><a href="projects.html">Projects</a></li>
                    <li><a href="tasks.html">Tasks</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <i class="fas fa-times" onclick="closemenu()"></i>
                </ul>
                <i class="fas fa-bars" onclick="openmenu()"></i>
            </nav>
            <div class="header-text">
                <!-- <p>UI/UX Designer</p> -->
                <h1>Hi, I'm <span>Dharmendra</span><br>From Bangalore</h1>
            </div>
        </div>
   </div> 
   <!---------------about-------------->
   <div id="about">
    <div class="container">
        <a name="About"></a>
        <div class="row">
            <div class="about-col-1">
                <img src="DR.webp">
            </div>
            <div class="about-col-2">
                <h1 class="sub-title">About Me</h1>
                <p>I'm a dedicated CSE-AI student known for my conscientiousness and organizational skills. Eager to kickstart my professional journey, I excel in rigorous coursework thanks to my strong work ethic and meticulous attention to detail. Ready to bridge theory with practice, I'm excited to contribute my CSE-AI expertise to dynamic workplaces and make a lasting impact.</p>
                
                <div class="tab-titles">
                    <p class="tab-links active-link" onclick="opentab('Skills')">Skills</p>
                    <p class="tab-links" onclick="opentab('Education')">Education</p>
                    <p class="tab-links" onclick="opentab('Experience')">Experience</p>
                </div>
                <div class="tab-contents active-tab" id="Skills">
                    <ul>
                        <li><span>Python</span><br>Building Codes by Understanding Algorithm</li>
                        <li><span>Web Development</span><br>Building a webiste using Html,Css amd JavaScript</li>
                        <li><span>Sql Database</span><br>Building Datebase and creating interface between webiste and database</li>
                    </ul>
                </div>
                <div class="tab-contents" id="Education">
                    <ul>
                        <li><span>2021-2025</span><br>BE at Sri Venkateshwara College of Engineering</li>
                        <li><span>2021</span><br>PUC at Reva Independent Pu College</li>
                        <li><span>2019</span><br>10th at Narayana E-Techno School</li>
                    </ul>
                </div>
                <div class="tab-contents" id="Experience">
                    <ul>
                        <li><span>2023</span><br>Internship at IBM SkillsBuild</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
   </div>
   <!---------------Services------------->
   <div id="services">
        <div class="container">
            <h1 class="sub-title">My Projetcs</h1>
            <div class="services-list">
                <div>
                    <i class="fa-solid fa-lock"></i>
                    <h2>Digital Keypad Security Door Lock</h2>
                    <p>The objective of this project is to create a secure and reliable door lock that can be opened using a digital 
                        keypad. The project aims to provide a cost-effective and practical solution for enhancing home security</p>
                    <a href="#">Learn more</a>
                </div>
                <div>
                    <i class="fa-solid fa-code"></i>
                    <h2>Implementation Of Binary Tree</h2>
                    <p>The implementation of a binary tree involves creating nodes, each with two child pointers, left and right. Operations include insertion, deletion, and traversal (in-order, pre-order, post-order). Recursive algorithms are commonly employed for these tasks. Binary trees find applications in data structures, search algorithms, and expression parsing, offering efficient data organization.</p>
                    <a href="#">Learn more</a>
                </div>
                <div>
                    <i class="fa-solid fa-chart-line"></i>
                    <h2>Mental Fitness Tracker</h2>
                    <p>A Python-based Mental Fitness Tracker harnesses AI to assess and enhance emotional well-being. It employs sentiment analysis on user-inputted thoughts, gauges mood trends, and recommends personalized activities. The system promotes self-awareness, providing insights into mental health patterns, fostering resilience, and suggesting interventions for a holistic approach to emotional fitness.</p>
                    <a href="#">Learn more</a>
                </div>
            </div>
        </div>
   </div>
   <!----------------Portfolio---------->
   <div id="portfolio">
        <div class="container">
            <h1 class="sub-title">My Tasks</h1>
            <div class="work-list">
                <div class="work">
                    <img src="quiz.webp">
                    <div class="layer">
                        <h3>Quiz App</h3>
                        <p>The Quiz App engages users with diverse questions, fostering knowledge and enjoyment through interactive challenges, making learning entertaining and accessible.</p>
                        <a href="#"><i class="fas fa-external-link-alt"></i></a>
                    </div>
                </div>
                <div class="work">
                    <img src="to-do.webp">
                    <div class="layer">
                        <h3>To-Do List</h3>
                        <p>A to-do list organizes tasks, enhances productivity, and aids in goal accomplishment by providing a clear roadmap for daily activities.</p>
                        <a href="#"><i class="fas fa-external-link-alt"></i></a>
                    </div>
                </div>
                <div class="work">
                    <img src="url shortner.webp">
                    <div class="layer">
                        <h3>Url Shortner</h3>
                        <p>URL shorteners condense long web addresses, enhancing convenience and sharing. They simplify links for social media and messaging platforms.</p>
                        <a href="#"><i class="fas fa-external-link-alt"></i></a>
                    </div>
                </div>
            </div>
            <a href="tasks.html" class="btn">See more</a>
        </div>
    </div>
    <!-------------------contact----------------->
    <div id="contact">
        <div class="container">
            <a name="contact"></a>
            <div class="row">
                <div class="contact-left">
                    <h1 class="sub-title">Contact Me</h1>
                    <p> <i class="fa-solid fa-paper-plane"></i>Dharmu17reddy@gmail.com</p>
                    <p ><i class="fa-solid fa-square-phone"></i>+91 9611241651</p>
                    <div class="social-icons">
                        <a href="https://www.facebook.com/profile.php?id=100013711693849" target="_blank"><i class="fa-brands fa-facebook"></i></a>
                        <a href="https://twitter.com/Dharmendra_17_" target="_blank"><i class="fa-brands fa-x-twitter"></i></a>
                        <a href="https://www.instagram.com/dharmendra__reddy/" target="_blank"><i class="fa-brands fa-instagram"></i></a>
                        <a href="https://www.linkedin.com/in/dharmendra-reddy-m-s-8289211b1/" target="_blank"><i class="fa-brands fa-linkedin"></i></a>
                        <a href="https://wa.me/+919611241651" target="_blank"><i class="fa-brands fa-whatsapp"></i></a>
                    </div>
                    <a href="My Resume.pdf" download class="btn btn2">Download CV</a>
                </div>
                <div class="contact-right">
                    <form>
                        <input type="text" name="Name" placeholder="Your Name" required>
                        <input type="email" name="Email" placeholder="Your Email Address" required>
                        <textarea name="Message"rows="6" placeholder="Your Message"></textarea>
                        <button type="submit" class="btn btn2">Submit</button>
                    </form>
                </div>
            </div>
        </div>
        <div class="copyright">
            <p>copyright DR.Made with <i class="fa-solid fa-heart"></i> by DR</p>
        </div>
    </div>

   <script>
    var tablinks=document.getElementsByClassName("tab-links");
    var tabcontents=document.getElementsByClassName("tab-contents");

    function opentab(tabname){
        for(tablink of tablinks){
            tablink.classList.remove("active-link");
        }
        for(tabcontent of tabcontents){
            tabcontent.classList.remove("active-tab");
        }
        event.currentTarget.classList.add("active-link");
        document.getElementById(tabname).classList.add("active-tab");
    }
   </script>

   <script>

        var sidemenu = document.getElementById("sidemenu");

            function openmenu(){
                sidemenu.style.right = "0";
            }
            function closemenu(){
                sidemenu.style.right = "-200px";
            }
   </script>
</body>
</html>
