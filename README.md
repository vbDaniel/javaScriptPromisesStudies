# JavaScript Promises and Async Programming

Estudos de JavaScript Promises(promise.js) and Async Programming(await.js)


Callback Pyramid of Doom: Um problema comum que surge qunado o programador usa muitos leveis hierárquica para acessar uma função (codigo sujo e de difícil reparo), por mais que uma função  assíncrona  esteja entre o código ela só será  chamada (callback) no final do processamento .


## How do Promises help?

Promise é um object que representa um eventual complemento ou falha de uma operação  assíncrona  e de seu valor resultante.

States:

- Pending (quando o promi
- se ainda está processando);
- Fulfilled (quando o promise completou com sucesso, retorna um unico valor);
- Rejected (retorna o porque foi rejeitado);
- Settled or Resolved(esta em Fulfiller ou Rejected, não esta mais pendente);

```JavaScript 
const readFile = file => new Promise((resolve, reject) =>{
  fs read file(file, (err, contents) => {
  if (err){
    reject(err)
  } else{
    resolve(contents)
  }
 })
})
readFile('./in1.txt')
  .then(contents => {
  console.log(String(contents))
  return readFile('./in2.txt')
  })
  .then(contents => {
    console.log(String(contents))
  })
```
Comsumo de API:

Objetos primordiais:
- Addresses;
- Items 
- Orders 
- Users 
- Items Categories 
- Order Statuses























