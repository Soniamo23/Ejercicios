MARKDOWN
RESUMEN DE REACT

En este trabajo vimos la implementacion del react.
Para instalar nos ayudamos con el comando "npm create vite"
React es una biblioteca realizada por facebook para hacer interfaces de usuario interactivas y dinamicas.

Son utilizadas para crear aplicaciones de una sola pagina
En base a ejercicios de una pagina llamada EXERCIMS poder introducir react a cada ejercicio
Tenemos dos ejemplos uno de ellos es :

const COLORS: string[] = ["black", "brown", "red", "orange", "yellow", "green", "blue", "violet", "grey", "white"];

function colorCode(color: string): number {
  const index: number = COLORS.indexOf(color.toLowerCase());
  if (index !== -1) {
    return index;
  } else {
    throw new Error("Color not found");
  }
}

function ColorPicker() {
  
  const [selectedColor, setSelectedColor] = useState<string>('');

  
  function handleColorChange(event) {
    const color = event.target.value;
    try {
      colorCode(color);
      setSelectedColor(color);
    } catch (error) {
      console.error(error .message);
    }
  }
  return (
    <div>
      <h2>Color Picker</h2>
      <label htmlFor="colorSelect">Select a color:</label>
      <select id="colorSelect" onChange={handleColorChange}>
        {COLORS.map((color, index) => (
          <option key={index} value={color}>{color}</option>
        ))}
      </select>
      <div style={{ marginTop: '20px', width: '200px', height: '200px', backgroundColor: selectedColor }}></div>
    </div>
  );
}

export default ColorPicker;


