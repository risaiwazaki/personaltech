{% include navigation.html %}

<--[Back to Home Page](/personaltech/)

## Final Deployment 

I deployed our site on swagketo.tk

{% include navigation.html %}

Raspberry Pi - Setting Up Java Web

# Discussion Questions/Policy
**Deployment: Every Friday 9pm**
**Policy: All work must be pushed by Thursday night, 24 hours  before deployment in order to be in the most updated pull**

# Deployment Guide
 ## Installing java runtime environment:
- [ ] $ sudo apt update 
- [ ] $ sudo apt upgrade
- [ ] $ sudo apt install default-jre 
- [ ] $ java -version 

 ## Install Java Development Kit
- [ ] $ sudo apt install default-jdk
- [ ] $ javac -version

 ## Maven is required to build project 
- [ ] $ sudo apt update 
- [ ] $ sudo apt upgrae

## Cloning repository:
- [ ] $ git clone https://github.com/ridhimainukurti/valid.git
- [ ] $ cd p1-Valid
- [ ] $ sudo mvn package

## Creating Web
- [ ] $ cd /etc/systemd/system/
- [ ] $ sudo nano p1-Valid.service
- [ ] $ sudo systemctl start p1-Valid
- [ ] $ sudo systemctl status p1-Valid

## Pulling Updated Code
- [ ] $ sudo git pull
- [ ] $ sudo mvn package 
- [ ] $ sudo java -jar/home/pi/pi-Valid/target/serving-web-content-0.0.1-SNAPSHOT.jar

## Run java project
- [ ] $ cd
- [ ] $ sudo java -jar/home/pi/pi-Valid/target/serving-web-content-0.0.1-SNAPSHOT.jar

## Obtaining Domain Name
- [ ]  [Step by Step Guide](https://docs.google.com/document/d/1nODveWp0jBzj4ZpFLgWCWTOXzLAHAPUhAQYmZJ4LhyU/edit)  

## Service File
- [ ] $ cd /etc/nginx/sites-available
- [ ] $ sudo ln -s /etc/nginx/sites-available/p1-Valid /etc/nginx/sites-enabled
- [ ] $ sudo nginx -t
- [ ] $ sudo systemctl restart nginx
- [ ] $ sudo nano /etc/systemd/system/valid.service

[Unit]
Description=Java
After=network.target

[Service]
User=pi
Restart=always
ExecStart=java -jar /home/pi/p1-Valid/target/csa-0.0.1-SNAPSHOT.jar

[Install]
WantedBy=multi-user.target 


- [ ] $ sudo systemctl start p1-Valid
- [ ] $ systemctl status p1-Valid
- [ ] $ sudo systemctl enable p1-Valid

# NGINX File
- [ ] $ sudo nano /etc/nginx/sites-available/p1-Valid

server {
    listen 80;
    server_name p1-valid.cf;

    location / {
        proxy_pass http://localhost:8080;
    }
}

## Test for no errors
- [ ] $ sudo ln -s /etc/nginx/sites-available/p1-Valid/etc/nginx/sites-enabled
- [ ] $ sudo nginx -t
- [ ] $ sudo systemctl restart nginx
- [ ] $ sudo systemctl start nginx
- [ ] $ sudo systemctl status nginx


# [Nginx running status](https://docs.google.com/document/d/1nXd7m8fAy-4cD54NTOrquUtCxx-63Auxtq0l2gP_tLg/edit)

# [Service Config](https://docs.google.com/document/d/1RbWeXaezjsGUvCkCHol9NRSxe7pB7SQd0DIPOGiKyfY/edit)

# [Port Forwarding Setting](https://docs.google.com/document/d/1ByeMHxUk8mbCJmzY6ohIreDKWV-0IOJGAaJpU1WV_oI/edit?usp=sharing)


# Resume Builder

I also worked on building our team's resume builder. 

Here is some front end code:

'''
<button type="button" class="btn btn-outline-dark">CREATE A NEW RESUME. we will help you create a resume step-by-step.</button>
        <button type="button" class="btn btn-outline-dark">I ALREADY HAVE A RESUME. we will re-format it and fill in your information so you don't have to. </button>

        <footer class="footer__copyright">
            <div class="container">
                <div class="row">
                    <div class="col-sm-6">
                        2022 © Linkdn.com. All Rights Reserved. | Call us at: 1 234 567 8901
                    </div>
                    <div class="col-sm-6">
                        <a href="/partners">Partners</a> |
                        <a rel="nofollow" target="_blank" href="/terms">Terms and Conditions</a> |
                        <a rel="nofollow" target="_blank" href="/privacy">Privacy Policy</a>
                    </div>
                </div>
            </div>
        </footer>
        
'''


Here is some back end code: 

'''

    private HWPFDocument openDocument(String file) throws Exception {
        URL res = getClass().getClassLoader().getResource(file);
        HWPFDocument document =  new HWPFDocument(new FileInputStream(location));                             
        return document;
    }

    private void saveDocument(HWPFDocument doc, String file) {
        try (
                FileOutputStream out = new FileOutputStream(file)) {
            doc.write(out);          
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
    public static String location;    
    static String file_loc1 = "./src/RESUME.doc";
    static String file_loc2 = "./src/RESUME2.doc";
}
'''

