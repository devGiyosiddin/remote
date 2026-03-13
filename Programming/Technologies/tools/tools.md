- Favicon error <link rel="shortcut icon" href="#">
- HTML form actions for test <!-- ?? action="<https://echo.htmlacademy.ru>" -->
- `````````
- ````````````````````````````````````.visually-hidden{`    
    `clip:rect(0 0 0 0);`    
    `clip-path:inset(50%);`    
    `height:1px;`   
    `overflow:hidden;`    
    `position:absolute;`    
    `white-space:nowrap;`    
    `width:1px;`    
}
- VS code SASS compiler settings
```
{
    "liveSassCompile.settings.formats": [
        {
            "format": "expanded",
            "extensionName": ".css",
            "savePath": "/css"
        },
        {
            "format": "expanded",
            "extensionName": ".min.css",
            "savePath": "/css"
        }
    ]
}
```

- Button hover
```css
@media (hover: hover) {
     button:hover {
         background-color: #fff;
     }
 }
 @media (hover: none) {
     button:active {
         background-color: #fff;
     }
 }
```
