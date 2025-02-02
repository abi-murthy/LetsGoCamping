## Brief Architecture Overview and Where Things Go
### React (Frontend)
All frontend code is to be located in `/site` or a subdirectory. `package.json` contains frontend build configuration and a list of packages your frontend needs to install in order to run. Place top-level pages in `/site/src/pages` and other components in `/site/src/components`.  You will need to download Node.js from https://nodejs.org/ to run the frontend code independently. 

### SpringBoot (Backend)
All backend code is located in `/src/main` or a subdirectory. Please do not remove `redirect()` from `SpringBootAPI.java`, as this is responsible for enabling your website files to be served. 

## Running Tests and Checking Coverage for Java & JavaScript

All unit tests will run with `mvn test`  and the coverage output directory will be `target/site/jacoco` for your Java code and `site/coverage` for your JavaScript code.

### Frontend
To run just your frontend tests:
- First, navigate in your terminal/command prompt to `/site`.
- Run `npm run test` to run Jest tests
  - This will ask you to select an option: `a` will run all tests, `f` will run failed tests, etc
- Run `npm run test -- --coverage --watchAll=false` to run Jest coverage tests. Note the extra `--` is required.


## Running Your App Locally During Development

To run the app in the development environment, first run `mvn compile` and then `mvn spring-boot:run` The app will now be available on `http://localhost:8080`

### Frontend only
- Navigate to `/site` in terminal/command prompt
- Run `npm start`. Note that this will auto rebuild/refresh when you make changes to the frontend.

### Backend only
- Run the main method in `SpringBootAPI.java`

## Running Acceptance Tests & Configuring a Subset of Features to Run

To run acceptance tests, use `mvn integration-test`.  Cucumber can be configured to run a subset of the features by modifying the `junit-platform.properties` file in the `src/test/resources` folder

## Useful Links & Resources
1. React
   - https://reactjs.org/tutorial/tutorial.html
   - https://reactjs.org/docs/react-api.html
   - https://reactjs.org/docs/hooks-intro.html
   - https://reactjs.org/docs/jsx-in-depth.html
   - https://www.w3schools.com/REACT/DEFAULT.ASP
2. Frontend Styling Libraries
   - https://tailwindcss.com/docs/guides/create-react-app
     - Start on Step 2 for installation
     - Search page for relevant styles/class names
   - https://getbootstrap.com/docs/5.3/getting-started/introduction/
     - Search page for relevant styles/class names
3. JavaScript unit testing with Jest
   - https://jestjs.io/docs/getting-started
   - https://jestjs.io/docs/tutorial-react
   - https://www.codecademy.com/learn/learn-react-testing
4. SpringBoot
   - https://docs.spring.io/spring-boot/docs/current/reference/html/index.html
5. Acceptance testing information
   - Gherkin information: https://cucumber.io/docs/gherkin/reference/
   - Cucumber information: https://cucumber.io/docs/cucumber/
   - Selenium information: https://www.selenium.dev/documentation/en/ 
   - Selenium Javadocs: https://www.selenium.dev/selenium/docs/api/java/
6. Java unit testing with JUnit
   - https://junit.org/junit5/
   - https://site.mockito.org/
   - https://www.eclemma.org/jacoco/trunk/doc/maven.html

