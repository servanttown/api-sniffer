# api-sniffer
An api sniffer library made by servant
![image](https://user-images.githubusercontent.com/94388882/223440199-e648a7d9-391c-444e-9350-909b0f138a01.png)

# How to use it?

Paste this inside of chrome developer console:

```
//an api sniffing library made by servant
const sniffer = {
    getAPI: async function() {
        let scripts = document.getElementsByTagName('script')

        for (let i = 0; i < scripts.length; i++) {
            const script = scripts[i].textContent
            const regex = /api/;
            const result = regex.exec(script)

            if (result !== null) {
                console.log('\nApi Found: ' + result.input)
            }
        }
    }
}

//run our sniffer
sniffer.getAPI()
```
