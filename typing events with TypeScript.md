When you need to read the value from the input event:

```tsx
const handleFilter = (e: ChangeEvent) => {  
  const value = (e.target as HTMLInputElement).value;  
  onFilterChange(value);  
};
```
