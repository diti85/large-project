## HouseHold

![household](https://github.com/diti85/large-project/assets/101580207/8dbd8c95-eecd-40f0-b8c2-1136a00fcc50)

HouseHold is a full-stack household management application that enables households to efficiently manage tasks, lists, and events in real-time, enhancing communication and collaboration among members. This repository contains the code for both the mobile app and the backend infrastructure.

# Features
 • Task Management: Create, assign, and track tasks within the household. Members can view their assigned tasks and mark them as complete.
 • List Management: Create and share lists, such as grocery lists or to-do lists, with other household members. Real-time updates ensure everyone stays in sync.
 • Event Management: Plan and organize events within the household. Invite members, set reminders, and track RSVPs.
 • Real-time Communication: Utilizes GraphQL and AWS Amplify to provide real-time updates and synchronization across all devices, fostering improved communication and collaboration.
 
## First Time Install

In the project directory, you can run:

### `npm install`

Also make sure you have the amplify-cli installed:
### `npm install -g @aws-amplify/cli`

Go to the Amplify Studio, click _Local setup instructions_ on the top
### `amplify pull --appId **** --envName ****`
Respond to the prompts like so:
```
? Choose your default editor: Visual Studio Code
? Choose the type of app that you're building (Use arrow keys)
? Choose the type of app that you're building javascript
Please tell us about your project
? What javascript framework are you using react
? Source Directory Path:  src
? Distribution Directory Path: build
? Build Command:  npm.cmd run-script build
? Start Command: npm.cmd run-script start
? Do you plan on modifying this backend? Yes
```

## Using the React App

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

## Development
### Frontend
When devloping a new feature that uses APIs, make sure to run `amplify pull` to retrieve the latest AWS config data.

For every other case: Develop the react application like normal, without making changes to the `amplify` folder.

### Backend
Make sure you run `amplify pull` before creating any new resources to make sure you have the latest AWS config data.
Use the Amplify CLI as needed to create resources and edit them.

In the case that resources are created through Amplify Studio instead of Amplify CLI (let's try to avoid this):

Make sure to run `amplify pull` after the resources are deployed, and create a Pull Request so GitHub has the most updated information.

## Testing

### `npm front:test`
### `npm back:test` (coming soon)

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.


## Troubleshooting
### Amplify Issues
If you haven't made any changes to Amplify and it's acting up, the surest way to resolve it is to delete the `amplify` folder, and run `amplify pull --appId **** --envName ****` again.
