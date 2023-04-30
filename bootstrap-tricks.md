# Bootstrap Tricks

## Break a paragraph without using the break tag. 
I like to use `d-block (display: block)` to push sentence to the next line. Below, on the `sm` it will display as two lines, but on `md` it will go back to a single line.

```
<h2 className="text-center">Three Skills <span className="d-block d-md-inline">I'm Grateful For</span></h2></Col>
```
### Live Sample
[jsohndata.github.io/neo-tokyo-portfolio#three-things](https://jsohndata.github.io/neo-tokyo-portfolio#three-things)

<br>

## Text alignment based on breakpoints
Various breakpoint will require differnt text alignment. Below, on `sm` the text will be centered `text-center (text-align: center)`. When it gets to `md` breakpoint it will change to `text-md-start (text-align: start)`.

```
<p className="text-center text-md-start">I am a team player who brings professional expertise, a positive attitude, and humor to keep the team energized, motivated, while delivering results.</p>
```

### Live Sample
[jsohndata.github.io/neo-tokyo-portfolio#three-things](https://jsohndata.github.io/neo-tokyo-portfolio#three-things)