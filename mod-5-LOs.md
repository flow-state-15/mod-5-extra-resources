<br>
These Learning Objectives are a supplement to App Academy Open and reinforce important concepts taught in Module 5.

<br>
<hr>
<br>


## JavaScript basics you will need know to succeed in Mod 5:

- How to destructure values from objects and arrays
  - Destructuring syntax:
    - `const { key } = object`
    - `const [ index1, index2 ] = array`
  - Purpose:
    - Destructuring is used everywhere in React and other modern libraries/frameworks
- How to use Ternaries
  - Ternary syntax:
    - `<condition> ? <truthy return> : <falsey return>`
  - Purpose:
    - To return different values depending on the outcome of the conditional expression
- How to use Logical Operators outside of boolean context
  - Logical Operator syntax:
    - `<truthy or falsey value> && / || / ?? <value to return>`
  - Purpose
    - They return the value of only one of the operands.
    - They are used for short-circuiting.
- How to create new keys in objects:
  - syntax:
    - `obj[newKey] = value`
- How to remove keys from objects:
  - syntax:
    - `delete object[key]`
- Know the difference between value types vs reference types in memory
  - Value Types:
    - Variables are stored containing an actual value
  - Reference Types:
    - Variables are stored and contain only a reference to the original object in memory that holds the value
- How to shallow copy vs deep copy an object
  - Shallow copy: `{...obj}`, `[...array]`
  - Deep copy: `JSON.stringify()` and `JSON.parse()`, up to a certain point. Best to use Lodash library.
  - What are the differences between a shallow copy and deep copy of an object?

**Complete the blanks in the section above**.
We will mention these concepts throughout Mod 5 with the expectation that you know how to implement them.
You **must** be fluent in the above concepts to succeed in this mod. Some of them are familiar to you, others not. No matter your current familiarity with the above concepts, take some time to look study them through Google, MDN or AppAcademy Open. Proficiency with these basics is absolutely vital to your career.

<br>
<hr>
<br>

### As you go through the lectures and material for each day, fill in the blanks below and take notes. Not every detail is covered in this file. It's up to you to fill out this document with what you've learned as well as important material from lectures and videos.

<br>

## Tuesday, W14, D2

React components, JSX and Routing

- **What is React**?:
  - Explanation: React is a JavaScript library that builds ui's through a declarative, component based approach.
- **What are React components**?:
  - Explanation: React components are functions that return JSX. Components can accept a props object as its only argument.
  - Syntax:
    ```
    function ReactComponent(props){
        return (
            <h1>Hello World</h1>
        )
    }
    ```
- **What is JSX**?
  - Explanation: JSX is a language made for react to enable declarative programming of ui. It is written like HTML and has similar tags. It uses the Babel compiler to convert this HTML-like syntax into JavaScript. Babel converts JSX into React functions.
  - Syntax: `<h1></h1>` and `<ReactComponent newKey={propValue}></ReactComponent>`
- **What are Component Props**?
  - Explanation: React components are functions, and react calls these functions with one argument: a props object. We can define new key value pairs in this props object within JSX.  Props keys are customarily deconstructed when the component is defined.
  - Syntax:
    ```
    function ReactComponent(propsObject){
        const { data } = propsObject
        return (
            <h1>{data}</h1>
        )
    }
    ```
- **What is React Router**?
  - Explanation: A library that keeps react components in sync with the url. It manages window location and dynamic route matching, and more.
  - Syntax:
    ```
    function App({ data }){
        return (
            <BrowserRouter>
                <Switch>
                    <Route exact path='/profile/:userId'>
                        <ProfileComponent data={data} />
                    </Route>
                </Switch>
            </BrowserRouter>
        )
    }
    ```
- **What is the useParams hook from React Router and how does it allow you to use parameters in your route? What does it return?**
  - Explanation: It enables you to extract wildcard values from your routes. `useParams()` returns an object with your parameter names as the key. We deconstruct the keys we need in our component.
  - Syntax: `const { userId } = useParams();`
- **What tools do you have to redirect a user**?
  - Explanation: Redirect component and useHistory hook
  - Syntax:
    ```
    function ProfileComponent({ user }){
        if(!user) return <Redirect to='/some/route' />
        // or
        const history = useHistory();

        const handleSubmit = (e) => {
            e.preventDefault();
            history.push('/new/page');
            }
        }
    ```

- **React documentation url**: [https://reactjs.org](https://reactjs.org)
- **React Router documentation url**: [https://v5.reactrouter.com/web/api/](https://v5.reactrouter.com/web/api/)
