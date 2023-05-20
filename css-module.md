# CSS Module
CSS Modules is a technique used in specific component or module, preventing style conflicts. When using CSS Modules, each CSS file is treated as a separate module. 

Traditional CSS operates on a global scope, which means that styles defined in one file can affect elements throughout the entire application. This can lead to unintended style overrides and conflicts, especially in larger projects. 

CSS Modules provide a solution to this problem by encapsulating styles within a specific component or module, making them local and isolated.

<br>

## Button.module.css
```
•custom-button { 
  font-size: 17px;  
  color: white;   
  background-color: blue;
}
```

## Button.js
```
import styles from ' ./Button.module.css';

function Button () {
  return (
    <button className={styles['custom-button']}>Open Modal</button>
  );

```