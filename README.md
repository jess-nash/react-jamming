# Jamming - A Codecademy React App
### Search for your favorite music and make a customized playlist
>In order to improve my skills with React.js, I undertook this capstone project with Codecademy.\
This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Features
#### With the help of the Spotify API, you can:
- search the Spotify library
- create a custom playlist
- save it to your Spotify account

You can view the live app [here](https://jam-master.surge.sh/).

## My Takeaways
### I gained a good grasp on how to:
  - create methods in my parent component (App.js), bind those methods, and pass them by assigning a child component an attribute with this.methodName as the value. `<Child attributeName={this.methodName}`
  - pass props to sibling components using this.prop.attributeName
  - create a module with methods that can get an access token, search a term in the serach bar, and save a playlist using an API.

## Challenges 
>(in regarding to React components and passing state)
- I created a method in the App component called `updatePlaylistName()` that accepted an argument of `name` and set the state of the playlist name to the input argument `name`.

- After creating (and binding) the updatePlaylistName method for the App component, I passed the method to the component Playlist as an attribute named `onNameChange`

- Next I created a method in the Playlist component called `handleNameChange()` . This method accepts an **event triggered** by the `onChange` attribute in the Playlist component’s `<input>` element. 

- It was a challenge to figure out how to use the `onNameChange()`attribute. It was passed from the App component, so I called it using `this.props.onNameChange()`. I was stuck on what to pass as the argument. Looking at the Playlist component’s `<input>` element, I had to use the value of the event target that is triggered by `onChange`, so I passed `event.target.value`, so `this.props.onNameChange(event.target.value)`. 

- So whenever a user begins to type in the `<input>` tag, the handleNameChange() method fires with the `event.target.value` which gives us access to the keys that are being typed. 

- And the method in App component onNameChange will update the state of the playlist name.

>(in regards to API implementation)
> I had a little bit of knowledge of HTTP request methods, but I became a bit lost when using `.fetch`, `.then`, and response.
> I'll have to do a bit more work with APIs to get a better understanding on how to use them.

## Run the app localy

In the project directory, you can run:

### `npm start`


Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.
