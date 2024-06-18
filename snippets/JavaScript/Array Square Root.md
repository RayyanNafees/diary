## Squaring an array

For Arranging a flat array into a nested rectagle of sub arrays

```ts
const squarray = array => {
	const sidelen   = Math.sqrt(array.length)
	const rowLength = Math.floor(sidelen)
	const length    = Math.ceil(sidelen)
	return Array.from({length}, 
	(_, n) => array
		.slice(n*rowLength, (n+1)*rowLength)
	)
}
```