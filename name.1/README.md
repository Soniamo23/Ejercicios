# EJEMPLO DE NAME

En este ejercicio fue con la implementacion de react

Este componente de React, TwoFer, es una función que recibe props. En este caso, espera una prop opcional llamada name, que es una cadena



## EJEMPLO

export function twoFer(name: string = "you"): string {
  return `One for ${name}, one for me.`;
}

## EJEMPLO CON REACT 

function App() {
  
  function twoFer(name: string = "you"): string {
    return `One for ${name}, one for me.`;
  }

  
  return (
    <div>
     
      <p>{twoFer("sonia")}</p>
      <p>{twoFer("Bob")}</p>
      <p>{twoFer()}</p>
    </div>
  );
}

export default App;

