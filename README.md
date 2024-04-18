# Exercício - Tabuada com JavaScript
## Codigo HTML:
```
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Tabuada</title>
</head>
<body>
    <header>
        <h1>Tabuada</h1>
    </header>

    <section>
        <div>
            <p>Número: <input type="number" name="num" id="txtn">
            <input type="button" value="Fazer Tabuada" onclick="tabuada()"></p>
        </div>
        <div id="res">
            <select name="sel" id="seltab" size="10">
                <option value="">Insira um número acima</option>
            </select>
        </div>
    </section>

    <footer>
        <p>&copy; Curso em video</p>
    </footer>
<script src="index.js"></script>
</body>
</html>
```

## Código CSS:
```
body{
    background-color: rgb(108, 108, 241);
    font: normal 15pt Arial;
}

header{
color:#fff;
text-align: center;
}

section{
background-color: #fff;
border-radius: 10px;
padding: 15px;
width: 500px;
margin: auto;
box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.488);
}

footer{
color:#fff;
text-align: center;
font-style: italic;
}

#res{
    text-align: center;
}
```

# Código JavaScript:
```
function tabuada(){
    let num = document.getElementById('txtn')
    let tab = document.getElementById('seltab')

    if(num.value.length == 0){
        window.alert('Por favor insira um número')
    } else {
        let n = Number(num.value)
        let c = 1
        tab.innerHTML = ''

        while(c <= 10){
            let item = document.createElement('option')
            item.text = `${n} x ${c} = ${n*c}`
            tab.appendChild(item)

            c++
        }
    }
}
```
