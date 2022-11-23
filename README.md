<div align="center">
	
# שאלות הכנה לראיון עבודה בReactJS אהבתם ? תנו ⭐
</div>


<div dir="rtl">
	
| מספר      | שאלה |
| ----------- | ----------- |
| 1   | [מה זה ריאקט?](#שמה-זה-ריאקט)       |
| 2   | [מה זה JSX?](#ש-מה-זה-jsx)       |
| 3   | [מהו הVirtual Dom ?](#ש-מהו-הvirtual-dom-)       |
| 4   | [איך עובד ה-Virtual DOM ?](#שאיך-עובד-ה-virtual-dom-)       |
| 5   | [איך מעבירים נתונים לקומפוננטות של ריאקט ](#שאיך-מעבירים-נתונים-לקומפוננטות-של-ריאקט-)       |
| 6   | [מה ההבדל בין state לprops?](#ש-מה-ההבדל-בין-state-לprops)   |
| 7   | [למה משמשים React Fragments ?](#שלמה-משמשים-react-fragments-)       |
| 8   | [מדוע לא מעדכנים state באופן ישיר ?](#ש-מדוע-לא-מעדכנים-state-באופן-ישיר-)       |
| 9   | [מדוע אנחנו צריכים key עבור רשימות בריאקט ?](#שמדוע-אנחנו-צריכים-key-עבור-רשימות-בריאקט-)       |
| 10  | [מהו state?](#ש-מהו-state)       |
| 11  | [מהו High Order Component ?](#ש-מהו-high-order-component-)       |
| 12  | [מהם Forms בריאקט ?](#שמהם-forms-בריאקט-)       |
| 13  | [מהם קומפוננטות בריאקט ?](#ש-מהם-קומפוננטות-בריאקט-)       |
| 14  | [מה ההבדל בין קומפוננטה שהיא Stateful ל Stateless ?](#ש-מה-ההבדל-בין-קומפוננטה-שהיא-stateful-ל-stateless-)       |
| 15  | [מהם HOOKS?](#ש-מהם-hooks)       |
| 16  | [מהו useState ?](#ש-מהו-usestate-)       |
| 17  | [מהו useEffect ואיך משתמשים בו ?](#ש-מהו-useeffect-ואיך-משתמשים-בו-)       |
| 19  | [מה השימוש בuseMemo() hook?](#ש-מה-השימוש-בusememo-hook)       |
| 20  | [מהו הuseRef Hook ואיך משתמשים בו ?](#ש-מהו-הuseref-hook-ואיך-משתמשים-בו-)       |
| 21  | [מהם Uncontrolled Compoonents ?](#ש-מהם-uncontrolled-compoonents-)       |
| 22  | [מהם Controlled Components ?](#ש-מהם-controlled-components-)       |
| 23  | [מנה את ההבדלים העיקריים בין Controlled Componenets לUncontrolled Components](#ש-מנה-את-ההבדלים-העיקריים-בין-controlled-componenets-לuncontrolled-components)       |
| 24  | [הסבר מהו Strict Mode בריאקט](#ש-הסבר-מהו-strict-mode-בריאקט)       |
| 25  | [מהם HOOKS מותאמים אישית (Custom Hooks) ?](#ש-מהם-hooks-מותאמים-אישית-custom-hooks-)       |
| 26  | [מה זה React Router ?](#ש-מה-זה-react-router-)       |







	
</div>

## ש.מה זה ריאקט?

ריאקט היא ספריית Javascript (לא פריימוורק) שנוצרה ע"י פייסבוק . ריאקט מאפשרת לנו לבנות ממשקי משתמש. 
ריקאט נוצרה על מנת לבנות עמוד יחיד (single-page) אבל ניתן ליצור איתה הכל - החל מאתרים סטטיים ועד אפליקציות למובייל בשימוש של אותם קונספטים.


## ש. מה זה JSX? 
ת.JSX מאפשר לנו לכתוב אלמנטים של HTML בתוך Javascript ולמקם אותם בDOM מבלי להשתמש בcreateElemet() ו/או appendChild().<br> 
JSX ממירה תגים של HTML לאלמנטים של ריקאט.<br>
נשים לב שהדפדפן אינו יכול להבין JSX לבדו ,ולכן אנחנו משתמשים בקומפיילר של Javascript שנקרא BABEL על מנת להמיר את הJSX לJavascript שהדפדפן מבין.


## ש. מהו הVirtual Dom ?

ת. הVirtual DOM (VDOM ) הוא רפרזנטציה של הDOM האמיתי בזכרון. הרפרזנטציה של ממשק המשתמש נשמרת בזכרון ומסתנכרנת עם הDOM האמיתי.זהו צעד שקורה בין הקריאה לפונקציה render לבין ההצגה של האלמנטים על המסך. כל התהליך נקרא reconciliation.

## ש.איך עובד ה-Virtual DOM ?
ת. הVirutal DOM עובד בשלושה צעדים פשוטים :

1.כאשר משתנים נתונים , כל ממשק המשתמש עובד רינדור מחדש בייצוג שלו בזכרון (VDOM)

<div align="center">

![image](https://user-images.githubusercontent.com/37695804/199983484-e756c056-9e0a-453a-a19f-864d21844542.png)


</div>


2.לאחר מכן השוני בין הייצוג החדש לישן מחושב

<div align="center">

![image](https://user-images.githubusercontent.com/37695804/199983930-26a0707b-abd0-4c4c-87fc-e21e74ac3e81.png)

</div>


3.לאחר שהסתיים החישוב , הDOM האמיתי יעדכן אך ורק את האלמנטים שהשתנו

<div align="center">

![image](https://user-images.githubusercontent.com/37695804/199984222-f204f4c5-32e7-46b2-80ee-d220504ea005.png)

</div>


## ש.איך מעבירים נתונים לקומפוננטות של ריאקט ? 

ישנם 2 דרכים עיקריות שמשמשות על מנת להעביר נתונים לקומפוננטות של ריקאט :


1.Props<br>
2.Context Api

Props הם נתונים המועברים מקומפוננטת הורה לקומפוננטת ילד , הם מוצהרים בקומפוננטת הילד , ניתן לקרוא להם בכל שם והם יכולים לקבל כל ערך ולידי

קומפוננטה של הורה :
```js
function Blog() {
  const post = { title: "My Blog Post!" };

  return <BlogPost post={post} />;
}

```
קומפוננטה של ילד:
```js
function BlogPost({ post }) {
  return <h1>{post.title}</h1>
}

```
מאחר וprops הם plain object properties אפשר לפרק אותם על מנת לגשת אליהם באופן ישיר :
```js
function BlogPost({ post }) {
  return <h1>{post.title}</h1>
}

```

כעת נעבור לContext , Context הוא בעצם data שמועבר מContext Provider לכל קומפוננטה שצורכת אותו , Context מאפשר לנו לגשת לנתונים בכל מקום בתכנית ( בהנחה שאנחנו מעבירים את הקונטקסט כפי שנראה בדוגמה ) , מבלי להשתמש בProps.
קונטקס הוא נתון שמועבר כלפי מטה על הvalue prop באמצעות Context.Provider.ניתן להשתמש בו באמצעות Context.Consumer או useContext הוק .

```js

import { createContext, useContext } from 'react';

const PostContext = createContext()

function App() {
  const post = { title: "My Blog Post!" };

  return (
    <PostContext.Provider value={post}>
      <Blog />
    </PostContext.Provider>
  );
}

function Blog() {
  return <BlogPost />
}

function BlogPost() {
  const post = useContext(PostContext)

  return <h1>{post.title}</h1>
}

```

## ש. מה ההבדל בין state לprops?

סטייטס (States) הם ערכים ( values ) שאנחנו יכולים **לקרוא ולעדכן** בקומפוננטות שלנו .
<br>
פרופס (props) הם ערכים שאנחנו מעבירים בין קומפוננטות ( בדר"כ מהורה לילד) . 

## ש.למה משמשים React Fragments ?

ת. React Fragments הם פי'צר מיוחד בריאקט המאפשר ל"קבץ" מספר אלנמטי ילדים ( children elements ) או קומפוננטות מבלי ליצור node נוסף בDOM
לעיתים קרובות אנחנו צריכים לכתוב מספר אלמנטים תחת הורה יחיד אך אנחנו לא רוצים להשתמש באלנט HTML גנרי כמו div .

נראה דוגמה , אם לצורך העניין נרצה ליצור טבלה , ללא Fragments זה יראה כך :

```js
function Table() {
  return (
    <table>
      <tr>
        <Columns />
      </tr>
    </table>
  );
}

function Columns() {
  return (
    <div>
      <td>Column 1</td>
      <td>Column 2</td>
    </div>
  );
}

```
אך נוכל לחסוך את הdiv בקומפוננטת הCoulmn ולכתוב כך :

```js

function Columns() {
  return (
    <>
      <td>Column 1</td>
      <td>Column 2</td>
    </>
  );
}

```

## ש. מדוע לא מעדכנים state באופן ישיר ?

ת. כי אם ננסה לעדכן סטייס באופן ישיר הקומפוננטה לא תתרנדר מחדש.

נניח שיש לנו את הסטייט הבא:

```js
[message,setMessage] = useState("");

```

```js
//טעות
message = 'Hello world'
```
במקום אנחנו נשתמש ב setMessage() , באופן הזה יתוזמן עדכון לסטייס של הקומפוננטה , ברגע שהסטייס ישתנה הקומפננטה תגיב ברנדור מחדש.


```js
//תקין
setMessage(`Hello world');

```


## ש.מדוע אנחנו צריכים key עבור רשימות בריאקט ?


ת.Keys הם ערכים מיוחדים שאנחנו חייבים להעביר לkey prop כאשר אנחנו משתמשים בפונקציית .map() על אלמנט או קומפוננטה , הkeys משמשים על מנת לזהות איזה מן הפריטים ברשימה השתנה , התעדכן או נמחק. במילים אחרות הkeys נועדו לתת זהות לכל אלמנט ברשימה וזאת על מנת שריאקט תוכל לעדכן את הDOM כהלכה , נראה דוגמה :

```js

posts.map(post => <li key={post.id}>{post.title}</li>)

```



## ש. מהו state? 

ת. state הוא אובייקט מובנה בריאקט שתפקידו לאחסן נתונים או אינפורמציה בנוגע לקומפוננטה , הstate יכול להשתנות במהלך התכנית , בכל שינוי שלו הקומפוננטה עוברת רנדור מחדש.

## ש. מהו High Order Component ?

ת. ידוע גם בתור HOC טכניקה מתקדמת לשימוש חוזר בלוגיקה של קומפוננטה. זוהי פונקציה שמקבלת קומפוננטה ומחזירה קומפוננטה חדשה.
סיבות להשתמש בHOC : 

* קל לתפעול
* אין צורך להעתיק את אותה הלוגיקה בכל קומפוננטה
* הופכת את הקוד לקריא יותר

## ש.מהם Forms בריאקט ? 

ת. ריאקט משתמשת בטפסים (forms) כדי לאפשר למשתמשים ליצור אינטרקציה עם אפליקציות ווב. 

* באמצעות טפסים משתמשים יכולים ליצור אינטרציה עם האפליקציה ולהזין את המידע הנדרש מתי שצריך. טפסים כוללים מספר אלמנטים כגון : שדות טקסט , כפתורים , checkboxes  , כפתורי רדיו וכו'
* טפסים משמשים למשימות רבות בינהם , אימות של משתמשים , חיפוש , פילטרינג וכו'

## ש. מהם קומפוננטות בריאקט ? 

ת. קומפוננטות הם אבני היסוד של יישומי ריאקט , אפליקצייה של ריקאט בד"כ כוללת מספר רב של קומפוננטות. קומפוננטה היא פיסה מממשק המשתמש. הקומפוננטות מחלקות את ממשק המשתמש לחלקים עצמאיים שניתן לבצע בהם שימוש חוזר וכן הם יכולים להיות מעובדים בנפרד.
יש שני סוגי קומפוננטות בריאקט - stateless component וStateful componenet.

## ש. מה ההבדל בין קומפוננטה שהיא Stateful ל Stateless ? 

ת. קומפוננטה שהיא Statefull היא קומפנטטה שמתחזקת סטייט כלשהו בעוד שקומפוננטה שהיא Stateless היא חסרת סטייט . 
נשים לב ששני הקומפוננטות יכולות לקבל Props.

## ש. מהם HOOKS?

ת. Hooks הוצגו לראשונה בגרסה 16.8 של ריאקט.
הHooks מאפשרים לקומפננטות פונקציונליות ( function componenets) לגשת לstate ולמטודות lifecycle בתוך הקומפוננטות , באופן עקרוני מגרסה זו אין צורך יותר בקומפוננטות מחלקה ( class componenets ) 

ה-hooks העיקריים הם:
useState<br>
useEffect<br>
useContext<br>
useReducer<br>
useRef<br>
useMemo<br>
useCallback<br>

נשים לב שניתן גם ליצור Hooks מותאמים אישית (custom hooks)

## ש. מהו useState ? 

ת.useState Hook  מאפשר לנו לעקוב/לנהל state בקומפוננטה פונקציונלית
נראה דוגמה : 

```js

  import React, { useState } from 'react';

 function Example() {
    const [count, setCount] = useState(0);

    return (
       <div>
          <p>You clicked {count} times</p>
          <button onClick={() => setCount(count + 1)}>
           Click me
          </button>
       </div>
);
 }

```



## ש. מהו useEffect ואיך משתמשים בו ? 


ת.useEffect Hook מאפשר לנו לבצע side effect בקומפוננטות שלנו 
דוגמאות לside effects : fetching data, עדכון הDOM באופן ישיר , timers .
<br>
useEffect מקבל שני ארגומנטים כאשר השני הוא ארגומנט אופציונלי.
הארגומנט הראשון הוא פונקציה שנקראת Effect , והארגומנט השני הוא מערך של תלויות ( dependencies ) כאמור הארגומנט הזה הוא אופציונלי ותכף נראה את השימוש בו.

```js

import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setTimeout(() => {
      setCount((count) => count + 1);
    }, 1000);
  });

  return <h1>I've rendered {count} times!</h1>;
}


```

הuseEffect רץ בכל רינדור , משמע שבדוגמה שלנו כאשר הcount משתנה מתבצע רינדור ( מאחר והשתנה הstate)
ולכן יופעל שוב הuseEffect שוב ישתנה הסטייט ולמעשה ניכנס ללופ אינסופי , מה הפתרון ? התלויות

כאשר לא מעבירים תלות : 

```js


useEffect(() => {
  //ירוץ בכל רינדור
});


```


כאשר מעבירים מערך ריק :

```js
useEffect(() => {
  //רץ ברינדור הראשון
}, []);



```

כאשר מעבירים prop או state:

```js
useEffect(() => {
  //רץ ברינדור הראשון
  //וגם כאשר הערך של הפרופ או הסטייס משתנים
}, [prop, state]);



```

## ש. מה השימוש בuseMemo() hook? 
ת. הuseMemo משמש לממואיזציה ( שינון ) של פונקציות יקרות כך שהם נקראות רק כאשר סט של קלטים משתנה ולא בכל רנדר. 
בדוגמה הבאה יש לנו פונקציה יקרה שרצה בכל רנדר , כאשר נוסיף משימה לtodo או נשנה את count יהיה דיליי בביצוע : 
```js

import { useState } from "react";
import ReactDOM from "react-dom/client";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);
  const calculation = expensiveCalculation(count);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <div>
      <div>
        <h2>My Todos</h2>
        {todos.map((todo, index) => {
          return <p key={index}>{todo}</p>;
        })}
        <button onClick={addTodo}>Add Todo</button>
      </div>
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
        <h2>Expensive Calculation</h2>
        {calculation}
      </div>
    </div>
  );
};

const expensiveCalculation = (num) => {
  console.log("Calculating...");
  for (let i = 0; i < 1000000000; i++) {
    num += 1;
  }
  return num;
};


```
כדי לפתור את הבעיה ניתן להתשמש בuseMemo שתשנן את הפונקציה "expensiveCount" , הuseMemo מקבל כפרמטר שני תלויות (dependencies) , הפונקציה היקרה תרוץ רק כאשר התלויות ישתנו . בדוגמה הבאה הפונקציה תרוץ רק כאשר count ישתנה ולא כאשר תתווסף משימה לtodos.
```js
import { useState, useMemo } from "react";
import ReactDOM from "react-dom/client";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);
  const calculation = useMemo(() => expensiveCalculation(count), [count]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <div>
      <div>
        <h2>My Todos</h2>
        {todos.map((todo, index) => {
          return <p key={index}>{todo}</p>;
        })}
        <button onClick={addTodo}>Add Todo</button>
      </div>
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
        <h2>Expensive Calculation</h2>
        {calculation}
      </div>
    </div>
  );
};

const expensiveCalculation = (num) => {
  console.log("Calculating...");
  for (let i = 0; i < 1000000000; i++) {
    num += 1;
  }
  return num;
};



```



## ש. מהו הuseRef Hook ואיך משתמשים בו ?

ת.Ref הוא בעצם Reference לDOM element  בריאקט , אנו יוצרים Refs באמצעות useRef Hook וניתן למקם אותם באופן מיידי בתוך משתנה , המשתנה הזה לאחר מכן מעובר לאלמנט של ריאקט על מנת לקבל רפרנס לאלמנט DOM ( כמו div,span וכו' ) , האלמנט עצמו והמאפיינים שלו כעת זמינים תחת המאפיין .current 
נראה דוגמה : 
```js

import { useRef } from 'react'

function MyComponent() {
  const ref = useRef();

  useEffect(() => {
    console.log(ref.current) // reference to div element
  }, [])

  return <div ref={ref} />
}


```

## ש. מהם Uncontrolled Compoonents ?
ת. Uncontrolled Components הם קומפוננטות שלא נשלטות ע"י הסטייט אלא ע"י הDOM. ולכן כדי לגשת לערכים שהוזנו אנחנו נצטרך להשתמש ברפרנסים(refs).

```js
import React, { useRef } from 'react';

function App() {
const inputRef = useRef(null);

function handleSubmit() {
	alert(`Name: ${inputRef.current.value}`);
}

return (
	<div className="App">
	<h3>Uncontrolled Component</h3>
	<form onSubmit={handleSubmit}>
		<label>Name :</label>
		<input type="text" name="name" ref={inputRef} />
		<button type="submit">Submit</button>
	</form>
	</div>
);
}

export default App;


```

## ש. מהם Controlled Components ?
ת. Controlled Components הן קומפוננטות שנשלטות ע"י הסטייט , כלומר הן לוקחות את הערך הנוכחי ומשנות אותו דרך פונקציות Callbacks כמו onClick וonChange.

```js
import { useState } from 'react';

function App() {
const [name, setName] = useState('');

function handleSubmit() {
	alert(`Name: ${name}`);
}
	
return (
	<div className="App">
	<h3>Controlled Component</h3>
	<form onSubmit={handleSubmit}>
		<label>Name:</label>
		<input name="name" value={name} onChange={(e) => setName(e.target.value)} />
		<button type="submit">Submit</button>
	</form>
	</div>
);
}

export default App;


```

## ש. מנה את ההבדלים העיקריים בין Controlled Componenets לUncontrolled Components

<div align="center">

| Controlled Component      | Uncontrolled Component |
| ----------- | ----------- |
| הקומפוננטה נשלטת ע"י הסטייט שלה      | הקומפוננטה נשלטת ע"י הDOM       |
| הקומפוננטות הללו צפויות , שכן כאמור הן נשלטות ע"י הסטייט   | הן בלתי צפויות מאחר שבמהלך מחזור החיים שלהן האלמטים יכולים לאבד את הרפרנס ואו יכולים להשתנות ולהיות מושפעים ממקורות אחרים        |
| יש להן שליטה טובה יותר על הערכים והנתונים בטפסים   | שליטה מאוד מוגבלת על הערכים והנתונים בטפסים        |

</div>


## ש. הסבר מהו Strict Mode בריאקט
ץת. StrictMode הוא כלי שהוסף לריאקט בגרסה 16.3 , מטרתו להדגיש בעיות פוטנציליות באפליקציה והוא מבצע בדיקות נוספות בשביל כך.
על מנת להפעילו יש לעטוף ב<React.StrictMode> : 
```js
function App() {
 return (
   <React.StrictMode>
     <div classname="App">
       <Header/>
       <div>
         Page Content
       </div>
       <Footer/>
     </div>
   </React.StrictMode>
 );
}

```

הStrictMode כרגע עוזר עם הבעיות הבאות :
* **מזהה קומפוננות בעלי מטודות מחזורי חיים (lifecycle) לא בטוחות** - 
	* מטודות מחזור חיים מסוימות אינן בטוחות בשימוש באפליקציות אסינכרוניות של ריאקט . בשימוש ספריות צד שלישי יש קושי להבטיח שהמטודות הללו אינן בשימוש.
	* הStrictMode עוזר לנו באמצעות כך שהוא מספק אזהרות אם קלאס קומפוננט משתמשת במטודות כאלה.
* **אזהרה לגבי שימוש בAPI ישן של סטרינגים** - 
	*  אם משתמשים בגרסה ישנה של ריקאט , callback ref היא הדרך המומלצת לנהל רפרנסים (refs) ולא string refs. הStrictMode יתן אזהרה אם נשתמש בstring ref כדי לנהל את הרפרנסים. 
* **שגיאה לגבי השימוש בfindDomNode:
	* בעבר , השיטה findDOMNode() שימשה כדי לחפש צומת בעץ הDOM , השיטה הזו הוצאה משימוש בריאקט , ולכן אם ננסה להתשמש בה הStrictMode יזהיר אותנו .
* שגיאה לגבי שימוש בContextAPI ישן.


## ש. מהם HOOKS מותאמים אישית (Custom Hooks) ?

ת. הוקס מותאמים אישית הם בעצם פונקציות JS שאחנו כותבים כדי לאפשר לעצמנו לחלוק את הלוגיקה של הקומפוננטה עם קומפוננטות אחרות , ובכך לחסוך כתיבת קוד מיותר.

לדוגמה נכתוב הוק בשם useFetch שיעזור לנו לעשות fetch לדאטה בתכנית .

ניצור את הקובץ useFecth.js

```js

import { useState, useEffect } from "react";

const useFetch = (url) => {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetch(url)
      .then((res) => res.json())
      .then((data) => setData(data));
  }, [url]);

  return [data];
};

export default useFetch;


```

שימוש בהוק החדש בindex.js 


```js

import ReactDOM from "react-dom/client";
import useFetch from "./useFetch";

const Home = () => {
  const [data] = useFetch("https://jsonplaceholder.typicode.com/todos");

  return (
    <>
      {data &&
        data.map((item) => {
          return <p key={item.id}>{item.title}</p>;
        })}
    </>
  );
};



```

יצרנו כאמור קובץ חדש בשם useFetch.js שמכיל פונקציה שנקראת useFecth שהיא מכילה את כל הלוגיקה שנדרשת על מנת לעשות fetch לנתונים , הפונקציה מקבלת url ומחזיר את הנתונים מממנו .

לאחר מכן בקובץ index.js אנחנו מייבאים את useFecth ומאתחלים אותו בדיוק כמו כל הוק אחר. נעביר לו את הurl הנדרש ונקבל בחזרה את הנתונים ממנו.



## ש. מה זה React Router ?

ת. ריקאט ראוטר היא ספרייה סטנדרטית שמשתמשים בה בריקאט על מנת לטפל בניתוב וניווט של עמודים/דפים באפליקצייה 
