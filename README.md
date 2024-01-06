# Modern Reactive Advertisement Page built using React, Vite, TailwindCSS. 

* Easy to edit data for clients who do not need to have knowledge of coding. Data is easy to edit and maintain in
constants/index.js file
* Responsive for all browsers
* Modernized web design practices for handling dynamic components and styles. 

PSA 
All credits to the owner and creator of this project @JavaScript Mastery on Youtube. To find more of this creator's projects and learn React and other technologies, check out <a href="https://github.com/adrianhajdin!">Github</a>

Key Points

* Tailwind is used to simply create elements and apply CSS to an entire project easily. 

* Designing Navbar: 
- The navbar component was designed with the intention of being able to dynamically add and create navLinks. navLink is an array predefined in our constants folder. We utilize the .map() function to create a 
<li> element for each of the navLinks "Home | About | Contact | Products | Reviews | </li> 
The children elements should share the same font and each have a key={nav.id}. This id prop should be set to the data-key of the element. We will use this to implement linking on our page to each of the respective navLinks 
* When designing elements that will be fit onto the end of the row or col, we should implement a margin of 0 after the last child element 
* Using media queries is made much simpler using Tailwind.css with built in classes like "sm:" "md:" "lg:" "xl:" "2xl": 
these are built in conditional operators: 
** Where this approach surprises people most often is that to style something for mobile, you need to use the unprefixed version of a utility, not the sm: prefixed version. Don’t think of sm: as meaning “on small screens”, think of it as “at the small breakpoint“. **
We used two react hooks to handle state: setActive and setToggle 
* Toggle is for handling the t|f for media queries 
* setActive handles which page we're on by checking if the current path matches any of our routes

* Designing Hero: 

We do not need a return statement for our Hero as we will render our component directly. 
Our Hero renders a section with the id="home" 
Our section has a flex container, on medium devices, it will flex-row and avg 
flex-col

A hero is designed with an opening sub heading, h1 element for large text, 
h1 element for our second line and p tag for description. 

Visualize how your constants data look and how  to re-use components.

* Designing Business.jsx
<section>
    <div className={layout.sectionInfo}>
            <h2 className={styles.heading2}> You do the business    
</section>

* Designing Button.jsx with intent of reuse

const Button = ({ styles }) => (
  <button type="button" className={`py-4 px-6 font-poppins font-medium text-[18px] text-primary bg-blue-gradient rounded-[10px] outline-none ${styles}`}>
    Get Started
  </button>
);

* Designing Business.jsx
first import the constants file we need for data for our features.
features is an array of objects. each object has 4 props: 
id, icon, title and content. 
We can destructure the object with an arrow function and iterate over each of the objects, creating a card for each. 

It really just is as simple as creating a div for each block element and a span for inline elements. There are many advantages to creating these cards dynamically such as inherited props, less code and easier maintainability. 

.feature-card:hover {
  background: var(--black-gradient);
  box-shadow: var(--card-shadow);
}

CSS property for the feature cards to change bg color when hovered adding a nice touch to UX.

Great static single page application for learning to use Tailwind.CSS, Vite.JS, React.JS, github pages.  