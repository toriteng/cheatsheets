# react!

### making components

```js
// a Person component that shows the person's name
// when you open { you are entering into Javascript }
function Person(props) {
    return <div style={fontSize:props.age}>
        {props.name}
    </div>
}
```

### use/render a component
```js
// here, you render the Person component
// and pass in the name "alice" in a prop (i.e. property, attrbute, argument)
<Person name = "alice />
```

### looping over components using .map(), which is a functiona as indicated by ()
```js
function App() {
    const people = ['Alice', 'Bob', 'Casey', 'Diana']
    return <div>
        {people.map((item, index) => {
            // you can name item and index anything you want but they are item and index ^^^
            // "key" is something that React needs
            return <Person key={index} name={item} />
        })}
    </div>
}
```

### useState
```js
// "state" lets you handle changes on your site
// in an intelligent way
function Counter() {
    const [const, setCount] = useState(0)
    return <button onClick={()=> setCount(count+1)}>
        You clicked me {count} times!
    </button>
}
```

### conditionally rendering components
```js
// you can use && to render a component based on some javascript condition
function App() {
    return <div>
        {1 + 1 == 2 && <WillRender />}
        {1 + 1 == 3 && <WontRender />}
    </div>
}

function App() {
    // called a ternary condition
    return <div>
        {1 + 1 == 2 ? <WillRender /> : <WontRender />}
    </div>
}
```