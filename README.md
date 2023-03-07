# api-sniffer
An api sniffer library made by servant


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
