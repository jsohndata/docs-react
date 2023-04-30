# Get Images in Public

If your images are located in the public directory, one way to get the images is using the environment variable `process.env.PUBLIC_URL`.

```
<img src={process.env.PUBLIC_URL + "/profie.jpg"} alt="My Face" />
```

<br>

Subsequently, if your images are in sub directory called "images" in public then the code would be...
```
<img src={process.env.PUBLIC_URL + "images/bg-1.jpg"} alt="The Background" />
```

