# FullStack Bank CICD

<img src="https://github.com/Harsh971/FullStack-Bank-CICD/blob/main/architecture.gif"></img>
![Preview](./screenshots/login.png)

## :page_with_curl: About


Full stack digital wallet application developed in Next.js and Node.js with TypeScript and built with Docker.

**Note:** the application is currently only in Brazilian Portuguese, I want to add an English translation soon.
<br />




## :man_technologist: Developed Skills

* Develop a frontend application with the Netx.js framework and TypeScript
* Use Sass and CSS Modules for frontend styling
* Develop a RESTful API in Node.js with Express.js and TypeScript
* Use an ORM
* Use a PostgreSQL database
* Document the API with Open API and the Swagger UI framework
* Implement backend integration tests using Mocha.js, Chai.js and Sinon.js with 100% coverage
* implement E2E tests with the Cypress framework in conjunction with the Testing Library
* Dockerize the application using Docker Compose
<br />

## :memo: Methodologies and paradigms

* Mobile First
* BEM (Block-Element-Modifier) ​​in CSS
* Object-Oriented Programming (OOP)
* SOLID Principles
<br />

## :hammer_and_wrench: Stacks

* TypeScript
* React.js
* Next.js
* Sass
* Cypress
* Testing Library
* Node.js
* Express.js
* Sequelize.js
* PortgreSQL
* Swagger UI
* Mocha.js
* Chai.js
* Sinon.js
* Docker
* Docker Compose

## Download Plugins : 
- `nodejs` : NodeJs Plugin
- `sonar` : SonarQube Scanner
- `owasp` : OWASP Dependency-Check
- `docker` : Docker, Docker Pipeline

## Configure Plugins : 
- Manage Jenkins > Global Tool Configuration

### Dependency-Check installations
- Name : DP
- Install Automatically > Install from github.com > dependency-check 6.5.1

### Docker installations
- Name : docker
- Install Automatically > Version (latest)

### NodeJs installations
- Name : node16
- Install Automatically > Version (16.20.2)

### SonarQube Scanner installations
- Name : sonar-scanner
- Install Automatically > Version (Default)

## Jenkinsfile Prerequisite : 
- for the stage named : *Trivy* we need to have trivy established into our Environmental System
```
sudo apt-get install wget apt-transport-https gnupg lsb-release

wget -qO - https://aquasecurity.github.io/trivy-repo/deb/public.key | gpg --dearmor | sudo tee /usr/share/keyrings/trivy.gpg > /dev/null

echo "deb (signed-by=/usr/share/keyrings/trivy.gpg) https://aquasecurity.github.io/trivy-repo/deb $(lsb_release -sc) main" | sudo tee -a /etc/apt/sources.list.d/trivy.list

sudo apt-get update

sudo apt-get install trivy -y
```

## Dockerfiles Locations : 

- /app/docker-compose.yml
- /Jenkinsfile
- /app/backend/Dockerfile
- /app/frontend/Dockerfile

## :hammer_and_wrench: Installation and execution

To run this application you need to have **Git**, **Docker**, **Node** and **Docker Compose** installed on your computer. Docker Compose needs to be version **2.5.0** or higher and Node version **16**.

In addition, to run the step-by-step commands below, your operating system must also have a **Bash terminal** installed. If you are using **Linux** or **macOS**, Bash is already installed by default. However, if your system is **Windows**, you may need to do [separate installation](https://www.lifewire.com/install-bash-on-windows-10-4101773).

### 1. In the project root directory, run the command below in the terminal to install the dependencies

```sh
npm install
```

### 2. Start the application containers

```sh
npm run compose:up
```

By running the command above, three containers will be started:

* ng_frontend - mapped on the port 3000
* ng_backend - mapped on the port 3001
* ng_db - mapped on the port 3002

They are the front-end, back-end and the database, respectively. After the containers starts, you can enter the <http://localhost:3000> address in your browser to see the application running.

To stop the containers, run the command below:

```sh
npm run compose:down
```

<br />

## :books: API Documentation

With the application running, access the <http://localhost:3001/docs> address in your browser to see the API documentation implemented with Swagger UI.
<br />

![API documentation/Documentação da API](./screenshots/api-docs.png)

## :test_tube: Tests

### Integration

I've implemented backend integration tests with 100% coverage. To check their result, just run the command below in the project root directory:

```sh
npm run test: integration
```

**Note:** to run the integration tests, it is not necessary for the application to be running, as the interaction with the database is mocked and the tests start an instance of the API before being started.
<br />

![Cobertura dos testes de integração](./screenshots/integration-coverage.png)

### E2E (End-to-End)

I've also implemented some E2E tests with the Cypress framework in conjunction with the Testing Library to use semantic selectors. **Applications must be running** before running E2E tests.

To open Cypress in the browser, run the command in the project root directory:

```sh
npm run test:e2e:open
```

A window will open with the list of specs, just click one of them to start the tests.

If you prefer, it is also possible to run the E2E tests without the graphical interface by using the command below:

```sh
npm run test:e2e
```

<br />

![Cypress](./screenshots/cypress.png)

### Run all tests

Run the command below in the project root directory tp run all integration and E2E tests in sequence in your terminal:

```sh
npm run test
```

**Note:** this command runs the E2E tests without the graphic interface.
<br />

## :iphone: Screenshots/Capturas de tela

![Login - mobile](./screenshots/login-mobile.png)
![Dashboard - mobile](./screenshots/dashboard-mobile.png)

![Dashboard](./screenshots//dashboard.png)

## Source Credits :
Original Source Code : [Click Here](https://github.com/raphaelalmeidamartins/fullstack-bank)
<br>
Tutorial Reference : [Click Here](https://www.youtube.com/watch?v=DIl2VcqZVdY&list=PLAdTNzDIZj_9C6qKZ3wE8t97OXqUZkzpB)

## Feedback

Your feedback is valuable! If you have suggestions for improving existing content or ideas for new additions, please open an issue or reach out to the repository maintainers. If you have any other feedbacks, you can reach out to us at harsh.thakkar0369@gmail.com


## Connect with Me
<p>

 <a href="https://twitter.com/HarshThakkar971" target="blank"><img align="center" src="https://img.freepik.com/premium-vector/vector-new-twitter-x-white-logo-black-background_744381-866.jpg" alt="HarshThakkar971" height="40" width="50" /></a>
  &nbsp;&nbsp;
  	<a href="https://linkedin.com/in/harsh-thakkar-7764bb1a4" target="blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/LinkedIn_logo_initials.png/800px-LinkedIn_logo_initials.png" alt="harsh-thakkar-7764bb1a4" height="40" width="40" /></a>
  &nbsp;&nbsp;
 <a href="https://instagram.com/harsh_thakkar09" target="blank"><img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Instagram_logo_2016.svg/768px-Instagram_logo_2016.svg.png" alt="harsh_thakkar09" height="40" width="40" /></a>
</p>


