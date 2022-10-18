# Week challenges (Monday) 💻

Time to catch up ⏱️

# Week challenges (Tuesday) 💻

Time to catch up ⏱️

# Week challenges (Wednesday) 💻

1. [x] [Watch this What Is React (React js) & Why Is It So Popular? video](https://www.youtube.com/watch?v=N3AkSS5hXMA)

Notes:

- A piece of User Interface (UI) - library created from Facebook since 2011
- We no longer have to write "addEventListener" and instead manipulate the DOM and updates it.
- Angular is more a framework solution.
- Whereas React only takes care of the view of the library. Views and syncs with sate for routing, HTTPS services and API to learn.

3. [x] [Watch this Learn React video](https://www.youtube.com/watch?v=hQAHSlTtcmY)

To review which version of NODE i have installed in my terminal:

```
node -v
```

To create a new react app:

```
npx create-react-app
```

To start creating

```
npm start
```

UUID Package install:

```
install UUID
```

This 30 minute video shows how to build the To-Do list project. Like a preview.

# Week challenges (Thursday) 💻

3. [x] React kata

```Typescript
import React from 'react';

export const EggList = ({eggs}) => {
  return (
    <ul>
      {eggs.map((egg, index) => {
      return <EasterEgg name={egg} key={index}/>
    })}
    </ul>
  )
};

export const EasterEgg = ({name}) => {
  return <li>{name}</li>
};

//componente: funcion de javascript, son unidades en React
//funcion: codigo de bloques que se puede llamar repetidas veces, pasa parametros y retorna algo
//un componente siempre retorna jsx
```
