# שאלות הכנה לראיון עבודה ריקאט


## ש.מה זה ריאקט?

ריאקט היא ספריית ג'אווהסקיפט(לא פריימוורק) שנוצרה ע"י פייסבוק . ריאקט מאפשרת לנו לבנות ממשקי משתמש. 
ריקאט נוצרה על מנת לבנות עמוד יחיד(single-page) אבל ניתן ליצור איתה הכל - החל מאתרים סטטיים ועד אפליקציות למובייל בשימוש של אותם קונספטים.


## ש. מה זה JSX? 
ת.JSX מאפשר לנו לכתוב אלמנטים של HTML בתוך JAVASCRIPT ולמקם אותם בDOM מבלי להשתמש בcreateElemet() ו/או appendChild().<br> 
JSX ממירה תגים של HTML לאלמנטים של REACT.<br>
נשים לב שהדפדפן אינו יכול להבין JSX לבדו ,ולכן אנחנו משתמשים בקומפיילר של ג'אווהסקריפט שנקרא BABEL על מנת להמיר את הJSX לג'אווהסקריפט שהדפדפן מבין.

## ש.איך מעבירים נתונים לקומפוננטות של ריאקט ? 

ישנם 2 דרכים עיקריות שמשמשות על מנת להעביר נתונים לקומפוננטות של ריקאט :


1.Props<br>
2.Context Api

Props הם נתונים המועברים מקומפוננטת הורה לקומפוננטת ילד , הם מוצהרים בקומפוננטת הילד , ניתן לקרוא להם בכל שם והם יכולים לקבל כל ערך ולידי

קומפוננטה של הורה :
```
function Blog() {
  const post = { title: "My Blog Post!" };

  return <BlogPost post={post} />;
}

```
קומפוננטה של ילד:
```
function BlogPost({ post }) {
  return <h1>{post.title}</h1>
}

```
מאחר וprops הם plain object properties אפשר לפרק אותם על מנת לגשת אליהם באופן ישיר :
```
function BlogPost({ post }) {
  return <h1>{post.title}</h1>
}

```

כעת נעבור לContext , Context הוא בעצם data שמועבר מContext Provider לכל קומפוננטה שצורכת אותו , Context מאפשר לנו לגשת לנתונים בכל מקום בתכנית ( בהנחה שאנחנו מעבירים את הקונטקסט כפי שנראה בדוגמה ) , מבלי להשתמש בProps.
קונטקס הוא נתון שמועבר כלפי מטה על הvalue prop באמצעות Context.Provider.ניתן להשתמש בו באמצעות Context.Consumer או useContext הוק .

```

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

```
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

```

function Columns() {
  return (
    <>
      <td>Column 1</td>
      <td>Column 2</td>
    </>
  );
}

```

## ש.מדוע אנחנו צריכים key עבור רשימות בריאקט ?


ת.Keys הם ערכים מיוחדים שאנחנו חייבים להעביר לkey prop כאשר אנחנו משתמשים בפונקציית .map() על אלמנט או קומפוננט , הkeys משמשים על מנת לזהות איזה מן הפריטים ברשימה השתנה , התעדכן או נמחק.במילים אחרות הkeys נועדו לתת זהות לכל אלמנט ברשימה וזאת על מנת שריאקט תוכל לעדכן את הDOM כהלכה , נראה דוגמה :

```

posts.map(post => <li key={post.id}>{post.title}</li>)

```

## ש. מהו הuseRef Hook ואיך משתמשים בו ?

ת.Ref הוא בעצם Reference לDOM element  בריאקט , אנו יוצרים Refs באמצעות useRef Hook וניתן למקם אותם באופן מיידי בתוך משתנה , המשתנה הזה לאחר מוכן מעובר לאלמנט של ריאקט על מנת לקבל רפרנס לאלמנט DOM ( כמו div,span וכו' ) , האלמנט עצמו והמאפיינים שלו כעת זמינים תחת המאפיין .current 
נראה דוגמה : 
```

import { useRef } from 'react'

function MyComponent() {
  const ref = useRef();

  useEffect(() => {
    console.log(ref.current) // reference to div element
  }, [])

  return <div ref={ref} />
}


```


