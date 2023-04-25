# Doc: React Router DOM

# Foundation

## Componets
* BrowserRouter
* Routes
* Route
* Link

## React Router DOM
A library that helps manage the application's routing logic by allowing developers to define routes and components to be rendered when specific URLs are accessed.

index.js
```
import { BrowserRouter } from 'react-router-dom';
~~~~~~~~
<BrowserRouter>
  <App />
</BrowserRouter>  
```

<br>

## Routes
Maintain and manages the routes in the application.

<br>

## Route
When a given path in the current URL is matched, React Router generates a new route and display a designated element on the page.

App.js
```
import { Routes, Route } from "React-Router-Dom";
import { About } from "./pages/about.js";
~~~~~~~~
<Routes>
  <Route path="/about" element={ <About /> } />
</Routes>
```

<br>

## Link
Navigate to a page without refreshing the current page

Nav.js
```
import { Link } from "React-Router-Dom";
~~~~~~~~
<nav>
  <Link to="/page">Page</Link>
</nav>
```

<br>
<br>

# Nested Routes

## Componets
* Outlet

Parent-Cateogry / Child-Category
eg) /music/beatles

app.js
```
Do this 👍
<Route path="/music" element={<Listing />} />
  <Route path="pixies" element={<Card />} />
  
Rather then...
<Route path="/music" element={<Listing />} />
<Route path="/music/pixies" element={<Card />} />
```

Once nested, use `<Outlet>` to display the child-category element within the parent-category component.

parent-category.js
```
import { Outlet, Link } from react-router-dom
~~~~~~~~
<h2>Parent Category</h2>
<ul>
  <li><Link to="child-category-1">Child 1</Link></li>
  <li><Link to="child-category-2">Child 2</Link></li>
  <li><Link to="child-category-3">Child 3</Link></li>  
</ul>
<Outlet />
```