# \<t-demo-atom\>

Using this component we can test the properties of component.

### Installation

```bash
    npm install --save nxtComponent/t-demo-atom
```

### References

```html
    <link rel="import" href="../../t-demo-atom/t-demo-atom.html">
```

### Simple Use

```html

    <t-demo-atom 
            el-name="t-button" 
            css-variables="button-primary-bg-color,button-primary-text-color" >
        
        <!--element to test-->
         <t-button class="primary" raised label="label"></t-button>

    </t-demo-atom> 

```

> Note - `el-name` value should be component tag name.  

#### Update default property value in setting section

```html
<t-demo-atom id="container"
            el-name="t-footer"  >
        
        <!--element to test-->
         <t-footer><t-footer>

    </t-demo-atom> 

    <script>

        var container = document.querySelector("#container");
        var elm = container.querySelector("t-footer")

        elm.sections = {
            name : "footer",

            links : [
                {
                    title : "About us",
                    href : "/aboutus"
                }
            ]
        };

        //Below method ensure the updated default value display in setting section
        container.refreshSetting();

    </script>
```
