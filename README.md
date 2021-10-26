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
O promisse alarga o codigo para baixo e nao para o lado formando uma pirâmide assim facilitando manutenção 
Comsumo de API:

Objetos primordiais:
- Addresses;
- Items 
- Orders 
- Users 
- Items Categories 
- Order Statuses


## async/await

Chamada sincrona é quando se espera o resultado em sequencia, JavaScript  é assíncrona  pois não  necessariamente vai aguardar pela resposta de uma linha.

Uma função  async é uma promisse que pode ser gerada em um formato diferente, possibilitando  dar um await na promisse então  facilita a manipulação  assíncrona.
```JavaScript 
const init = async() => {
  try{
  const contents = await readFile('./in1.txt')
  const contents2 = await readFile('./in2.txt')
  console.log(String(contents))
  console.log(String(contents2))
  }catch(err){
    console.log(err)
  }
}  
```

A ideia do async/await é dar ao JavaScript uma função sincrona mais completa;






















