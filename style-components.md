*introductions*

*instalacion*

*uso*
- `import styled from 'styled-components'`
- una ves importado generamos una constante
```js
const Button = styled.button`
	width:5rem;
	background-color:#98ca#f;
	border:none;
	border-radius:10px;
	color:${props=>props.color};
	&:hover {
		transform:scale(1);
	}
` 
<Button color="gray">Comprar</Button>

/*const de colores globales para la app*/
export const colors ={
	green:"#98ca3f",
	orange:"f8b71c"
}

```
