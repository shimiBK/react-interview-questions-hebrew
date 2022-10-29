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
פרופס (props) הם ערכים שאנחנו מעבירים בין קומפוננטות . 


