JSX (JavaScript XML) is a syntax extension for JavaScript, commonly used with React, that allows for writing UI components using a syntax resembling HTML, which then gets transcompiled to regular JavaScript.

TSX (TypeScript XML) is an extension of TypeScript that enables developers to write JSX syntax within TypeScript files, allowing for the creation of React components with the added benefits of type-checking and strong typing features.

<br>

---

<br>


## Introduction to Function Components

<br>

A component in React can be defined using either functions or classes. Here's a basic functional component:

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

<br>

#### Basic Usage

To use the `Welcome` component, you'd include it in JSX like so:

```jsx
<Welcome name="Tony Stark" />
```

<br>

---

<br>

## Props in React

<br>

`props` (short for "properties") are a way of passing data from parent to child components. They are read-only and help to make your components reusable.

<br>

#### Passing and Using Props

Given our `Welcome` component, if we want to greet different people:

```jsx
function App() {
  return (
    <div>
      <Welcome name="Tony Stark" />
      <Welcome name="Steve Rogers" />
      <Welcome name="Thor Odinson" />
    </div>
  );
}
```

<br>

---

<br>

## Destructuring Props in Components

<br>

In modern React, it's common to see component props being destructured right in the function parameters. This makes the code cleaner and allows direct access to these props without needing to prefix them with `props.`.

<br>

#### Example Without Destructuring

```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

<br>

#### Example With Destructuring

```jsx
function Welcome({ name }) {
  return <h1>Hello, {name}</h1>;
}
```

<br>

Both components work the same way, but in the latter, `name` is pulled directly from the `props` object.

<br>

---

<br>

## Multiple Props and Children

<br>

`children` is a special prop in React that allows components to accept and display child content.

```jsx
function Card({ title, children }) {
  return (
    <div className="card">
      <h2>{title}</h2>
      <div>{children}</div>
    </div>
  );
}
```

<br>

#### Usage

```jsx
<Card title="My Card">
  This is some content inside the card.
</Card>
```

<br>

Here, the `Card` component is expecting a `title` prop and also any child content passed between the opening `<Card>` and closing `</Card>` tags. This child content is accessed using the `children` prop.

Destructuring can also be used with nested properties, default values, and in many other contexts in JavaScript, not just React. It's a valuable ES6 feature to understand and utilize.

<br>

---

<br>

## 3. Component Composition

<br>

Components can be composed together to create more complex UIs.


<br>

#### Example: A User Info Component

Let's say we have a `ProfilePicture` and a `ProfileLink` component:

```jsx
function ProfilePicture(props) {
  return <img src={props.src} alt={props.name} />;
}

function ProfileLink(props) {
  return <a href={props.link}>{props.name}</a>;
}
```

<br>

We can create a `UserInfo` component that combines the above two:

```jsx
function UserInfo(props) {
  return (
    <div>
      <ProfilePicture src={props.user.imgSrc} name={props.user.name} />
      <ProfileLink link={props.user.profileLink} name={props.user.name} />
    </div>
  );
}
```


<br>

#### Usage

To use the `UserInfo` component:


```jsx
const user = {
  name: 'Sarah',
  imgSrc: 'path_to_image.jpg',
  profileLink: 'https://example.com/sarah'
};

function App() {
  return <UserInfo user={user} />;
}
```

<br>

---

<br>

## Final Acknowledgements 

**Note**: Always start component names with a capital letter. React treats components starting with lowercase letters as DOM tags.
