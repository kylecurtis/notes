TSX (TypeScript XML) is an extension of TypeScript used primarily with React, enabling developers to write UI components with a syntax that resembles HTML, complemented by TypeScript's strong typing features, which then gets transcompiled to regular JavaScript.

<br>

---

<br>

## Introduction to Function Components

<br>

A component in React can be defined using either functions or classes. Here's a basic functional component in TSX:

```tsx
function Welcome(props: { name: string }) {
  return <h1>Hello, {props.name}</h1>;
}
```

<br>

#### Basic Usage

To use the `Welcome` component, you'd include it in TSX like so:

```tsx
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

```tsx
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

```tsx
function Welcome(props: { name: string }) {
  return <h1>Hello, {props.name}</h1>;
}
```

<br>

#### Example With Destructuring

```tsx
function Welcome({ name }: { name: string }) {
  return <h1>Hello, {name}</h1>;
}
```

Both components work the same way, but in the latter, `name` is pulled directly from the `props` object.

<br>

---

<br>

## Multiple Props and Children

`children` is a special prop in React that allows components to accept and display child content.

```tsx
interface CardProps {
  title: string;
  children: React.ReactNode;
}

function Card({ title, children }: CardProps) {
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

```tsx
<Card title="My Card">
  This is some content inside the card.
</Card>
```

<br>

---

<br>

## Component Composition

<br>

Components can be composed together to create more complex UIs.

<br>

#### Example: A User Info Component

Let's say we have a `ProfilePicture` and a `ProfileLink` component:

```tsx
interface ProfilePictureProps {
  src: string;
  name: string;
}

interface ProfileLinkProps {
  link: string;
  name: string;
}

function ProfilePicture(props: ProfilePictureProps) {
  return <img src={props.src} alt={props.name} />;
}

function ProfileLink(props: ProfileLinkProps) {
  return <a href={props.link}>{props.name}</a>;
}
```

We can create a `UserInfo` component that combines the above two:

```tsx
interface User {
  name: string;
  imgSrc: string;
  profileLink: string;
}

interface UserInfoProps {
  user: User;
}

function UserInfo(props: UserInfoProps) {
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

```tsx
const user: User = {
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

---

In this version, I added TypeScript type annotations to make the code TSX-compatible, providing static type checking and better code clarity.
