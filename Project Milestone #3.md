<!DOCTYPE html>

<html lang="en">
<head>
    <title>DNS</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
    <link rel="stylesheet" href="style.css">
    <style>
        body {
            font-family: Ariel, sans-serif;
            background-color: #f4f4f4;
            line-height: 1.6;
            padding-top: 50px;
        }
        .container {
            margin-top: 20px;
        }
        h1, h2, h3 {
            word-wrap: break-word;
            color: #333;
        }
        .footer {
            background-color: #f8f8f8;
            padding: 20px 0;
            text-align: center;
        }
        .results {
            margin-top: 20px;
            font-weight: bold;
        }
        img {
            margin-top: 20px;
            border-radius: 50%;
        }
        @media (max-width: 618px) {
            .nav-tabs > li > a {
                text-align: center;
            }
            .tab content {
                padding: 15px; 
            }
            footer .alert {
                font-size: 14px;
            }
            .form-control {
                width: 100%;
                margin-bottom: 10px;
            } 
        @media (min-width: 720px) and (max-width: 900px) {
            .nav-tabs > li > a {
                text-align: left;
            }
            .tab-content {
                padding: 20px;
            }
            footer .alert {
                font-size: 16px;
            }
            .form-control {
                width: 50%;
                margin-bottom: 10px;}
        @media (min-width: 901px) {
            .nav-tabs > li > a {
                text-align: left;
            }
            .tab-content {
                padding: 30px;
            }
            footer .alert {
                font-size: 18px;
            }
            .form-control {
                width: 30%;
                margin-bottom: 10px;
            }
        }
    }
}
    </style>
</head>
<body>
<!--Creating tabs for Homepage, Types, Orgin, and References-->
<div class="container">
    <h1>DNS</h1>
    <ul class="nav nav-tabs">
        <li class="active"><a data-toggle="tab" href="#Homepage">Homepage</a></li> 
        <li><a data-toggle="tab" href="#Types">Types</a></li>
        <li><a data-toggle="tab" href="#Origin">Origin</a></li>
        <li><a data-toggle="tab" href="#Quiz">Quiz</a></li>
        <li><a data-toggle="tab" href="#References">References</a></li>
    </ul>
    <div class="tab-content">
        <div id="Homepage" class="tab-pane fade in active">
            <h2>Executive Summary</h2>
                <p>Domain Name Server (DNS) is a form of heirarchy that prioritizes on naming systems of computers, addresses, and other devices that share a connection on the Internet.
                 If a user, for instance, attempts to access walmart.com, the server will allow them to simply search up "walmart.com" on the URL instead of "23.39.184.192" which is the IP address of the site.
                </p>
<!--Creating a bulletin list of Key Terms-->
            <h2>Key Terms</h2>
            <p>
                <ul>
                    <li><strong>Domain Name System (DNS)</strong></li>
                    <li><strong>Root Server</strong> </li>
                    <li><strong>TLD (Top-Level Domain)</strong> </li>
                    <li><strong>Resolving Name Server</strong> </li>
                    <li><strong>Organizational Hieracrchy</strong> </li>
                    <li><strong>Geographical Hierarchy</strong> </li>
                    <li><strong>Paul Mockapetris</strong> </li>
                    <li><strong>BIND</strong> </li>
                </ul>
            </p>
        </div>
<!--Creating a tab for Types of DNS-->
<!--The tab transitions to a fade animation when clicked-->
        <div id="Types" class="tab-pane fade">
            <div class="contianer">
            <h2>Types of DNS</h2>
                <p>The DNS system contains three main types of servers that are queried by the DNS query. Those servers include:</p>
                <div class="media-body">
                    <h3 class="media-heading"><strong>Root Servers:</strong></h3> <!--This command makes the title bold-->
                    <p>The role of a Root Server is to recieve and answer requests for information regardng TLD servers
                        Controlled by the Internet Corporation for Assigned Names and Numbers (ICANN), root servers do not obtain information for where 
                        the domain is hosted. However, they are able to direct the requester to the name of the servers that handle the hosted TLD. 
                        For example, if a user requests "google.com", the DNS server will not be able to find the website's IP address.
                        However, the root server will be able to direct the user and DNS server to the TLD name server which is the ".com" domain.
                    </p>
                    <h3 class="media-hearing"><strong> TLD Name Servers</strong></h3>
                    <p>
                        While the root server recieves the requests from the website domain, the server will send it to a ceratin TLD name sever based on the TLD name.
                        Then, the server will release the IP address of the website and foward the query to the DNS to continue the process of bringing up the website.
                        For instance, if a user was browsing "www.walmart.com", the IP address would be saved in the second domain via the top domain.
                        There are two types of heirarchies within the domain: georgraphical and organizational. 
                        <ul>
                        <li><dt>Geographical hierarchy:</dt></li>
                        <dd>It focuses on the domain names based on different localized areas in the world. For example, ".org.us" is a top level domain that target organizations in the United States.</dd>
                        <li><dt>Organizational hierarchy:</dt></li>
                        <dd>It defines the purpose of the top level domain name.</dd>
                        </ul>
                    </p>
                    <h3 class="media-heading"><strong>Resolving Name Servers</strong></h3>
                    <p>
                        Similar to DNS, resolving name server act as a translator and transcribe domain names into IP adresses.
                        In addition, they are configured by an ISP (internet service provider) and other third party organizaions to direct the user to the website.
                        Resolving name servers are useful for dialup, cable modems, ADSL, DSL, VPN and similar users.
                        It also allows users to access the internet without having to remember the IP address of the website.
                    </p>
                </div>
            </div>
        </div>
        <div id="Origin" class="tab-pane fade">
            <h2>Origin of DNS</h2>
            <p>
                In 1983, Paul Mockapetris and his team was in charge of establishing a server that would allow users to
                browse throughout the internet without needing to rememnber certain IP addresses.
                Prior to the DNS, users had to use HOST.TXT files that mapped hostnames to IP address.
                However, because the variety of newly developed websites were increasing exponentially at the time,
                Mockapetris created the DNS to provide more efficiency and simplicity for users.
            </p>
<!--Adding an image of Paul Mockapetris-->
            <div class="row">
                <div class="col-md-12 col-md-offset-0">
            <img class="img-responsive" src="data:image/jpeg;base64,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" alt="Paul Mockapetris" 
            width ="150" height="150">
<!--Adding a caption below the Paul Mockapetris image-->
            <div class="caption">
                <p>
                    "DNS was created to let people use names for anything. But they had to 
                    figure out how to organize the distribution of domain names and how to 
                    ensure the system could accommodate diversity without unnecessary restrictions." 
                    <p>-Paul Mockapetris"</p>
                </p>
            </div>
            </div>
            <h3><strong>BIND</strong></h3>
            <p>
                By 1984, students and professionals at the University of California 
                developed an additional software system known as BIND (Berkeley Internet Name Domain).
                It was written to serve as an implementation of domain name servers as well as a reference architecture 
                for the server. In addition, BIND was designed to provide all DNS-related server functions as well as run caching 
                DNS servers and authoritative servers. The software evolved and developed more throughout the 
                years by contributions from the Internet Software Consortium (ISC) and other organizations.
            </p>
            </div>
        </div>
        <div id="References" class="tab-pane fade"> 
            <h2>References</h2>
            <ul>
                <li>Fisherm Tim. October 17, 2023, DNS Servers: What Are They and Why Are They Used? https://www.lifewire.com/what-is-a-dns-server-2625854"</li>
                <p> </p>
                <li>Ellingwood, Justin. November 4, 2020. An Introduction to DNS Terminology, Components,
and Concepts. https://www.digitalocean.com/community/tutorials/an-introduction-todns-terminology-components-and-concepts
</li>
                <p> </p>
                <li>DNSMap. 2024. What Are Top Level Domain (TLD) Name Servers?
https://dnsmap.io/articles/what-are-top-level-domain-(tld)-name-servers</li>
                <p> </p>
                <li>DNS GEEK. August 17, 2009. What Is Resolving Name Server?.
https://www.dnsknowledge.com/whatis/resolving-name-server/</li>
                <p> </p>
                <li>Petrova, Beloslava. March 18, 2025, DNS history. When and why was DNS created?
https://www.cloudns.net/blog/dns-history-creation-first/</li>
                <p> </p>
                <li>Buxton, Chris. June 8, 2023. All About BIND DNS: Who, How, & Why.
https://www.pluralsight.com/resources/blog/cloud/all-about-bind-dns-who-how-why</li>
                <p> </p>
                <li>Internet Systems Consortium. 2024. BIND 9: Versatile, classic, complete name server
software.
https://www.isc.org/bind/</li>
            </ul>
        </div>
<!--Creating a tab for the quiz-->        
        <div id="Quiz" class="tab-pane fade">
            <h2>Quiz</h2>
            <p>Test your knowledge of DNS with the following questions:</p>
<!--Creating a multiple choice question-->
            <h5>1: What does DNS stand for?:</h5>
                <div class="form-check">
                 <input class="form-check-input" type="radio" name="Form1" id="form1Option1" value="option1">
                 <label class="form-check-label" for="form1Option1">
                     Domain Name System
                </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form1" id="form1Option2" value="option2">
                    <label class="form-check-label" for="form1Option2">
                        Domain Network Service
                 </label>
                 </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form1" id="form1Option3" value="option3">
                    <label class="form-check-label" for="form1Option3">
                        Domain Name Server 
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form1" id="form1Option4" value="option4">
                    <label class="form-check-label" for="form1Option4">
                        Data Network System
                    </label>
                </div>

            <h5>2: Who created DNS?</h5>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form2" id="form2Option1" value="option1">
                    <label class="form-check-label" for="form2Option1">
                      Paul Mockapetris
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form2" id="form2Option2" value="option2">
                    <label class="form-check-label" for="form2Option2">
                        Paul Rudd
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form2" id="form2Option3" value="option3">
                    <label class="form-check-label" for="form2Option3">
                        Steve Jobs
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form2" id="form2Option4" value="option4">
                    <label class="form-check-label" for="form2Option4">
                        Tim Berners-Lee
                    </label>
                </div>
            <h5>3: Who created BIND?</h5>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form3" id="form3Option1" value="option1">
                    <label class="form-check-label" for="form3Option1">
                        Harvard University
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form3" id="form3Option2" value="option2">
                    <label class="form-check-label" for="form3Option2">
                        University of California
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form3" id="form3Option3" value="option3">
                    <label class="form-check-label" for="form3Option3">
                        Kennesaw State University
                    </label>
                </div>
                <div class="form-check">
                    <input class="form-check-input" type="radio" name="Form3" id="form3Option4" value="option4">
                    <label class="form-check-label" for="form3Option4">
                        None of the above
                    </label>
                </div>
            <h5>4: What are the types of heirarchies in the root server?</h5>
                <div class="form-check">
                    <label class="form-check-label" for="check1">
                        <input class="form-check-input" type="checkbox" name="check1" id="check1" value="option1">
                        Geographical
                    </label>
                </div>
                <div class="form-check">
                    <label class="form-check-label" for="check2">
                        <input class="form-check-input" type="checkbox" name="check2" id="check2" value="option2">
                        Logical 
                    </label>
                </div>
                <div class="form-check">
                    <label class="form-check-label" for="check3">
                        <input class="form-check-input" type="checkbox" name="check3" id="check3" value="option3">
                        Optional
                    </label>
                </div>
                <div class="form-check">
                    <label class="form-check-label" for="check4">
                        <input class="form-check-input" type="checkbox" name="check4" id="check4" value="option4">
                        Organizational
                    </label>
                </div>  
                <div class="form-check">
                    <label class="form-check-label" for="check5">
                        <input class="form-check-input" type="checkbox" name="check5" id="check5" value="option5">
                        Confidential
                    </label>
                </div>
<!--Creating a fill in the blank for the last question-->
                <h5>5: What year was DNS created?</h5>  
                    <div class="form-group">
                        <input type="text" class="form-control" id="yearInput" placeholder="Enter the year">    
                    </div>
<!--Creating a button to submit the quiz-->
                <button type="Submit" class="btn btn-primary" >Submit</button>
<!--Creating a div to show the results of the quiz-->
                <div class="results">Your score is: <span id="score">0</span></div>
                <script>
                    document.querySelector('button[type="submit"]').addEventListener('click', function(event) {
                        event.preventDefault(); 
                        let score = 0;

                        if (document.getElementById('form1Option3').checked) score++;
                        if (document.getElementById('form2Option1').checked) score++;
                        if (document.getElementById('form3Option2').checked) score++;
                        if (document.getElementById('check1').checked && document.getElementById('check4').checked) score++;
                        if (document.getElementById('yearInput').value === '1983') score++;
                        document.getElementById('score').textContent = score;
                        if (score >= 4) {
                            alert('Congratulations! You scored ' + score + ' out of 5! Way to go!');
                        } else {
                            alert('You scored ' + score + ' out of 5. Try again!');
                        }
                    });
                </script> 
<!--Creating a button to show the answers-->
                <button type="button" class="btn btn-info" data-toggle="collapse" data-target="#quizAnswer">Show Answers</button>
                <div id="quizAnswer" class="collapse">
                    <ul>
                        <li>1. Domain Name System</li>
                        <li>2. Paul Mockapetris</li>
                        <li>3. University of California</li>
                        <li>4. Geographical and Organizational</li>
                        <li>5. 1983</li>
                    </ul>
                </div>
                <button type="Restart" class="btn btn-secondary" onclick="location.reload();">Restart Quiz</button>
            </div>
        </div>         
    </div>
</div>
</div>
<!--Creating a footer for the page-->
<!--The footer contains a link to the class website-->
<footer class="footer">
    <div class="container">
        <div class="alert alert-info">
        <p class="text-info">This is a class project <a href="#" class="alert-link">https://ksuweb.github.io/IT3203/</a></p>
    </div>
        </div>
</footer>
</body>
</html>

