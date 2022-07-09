Here we use this subcomponent to easily pass the icons we need to the left [[Sidebar]] neatly using [[destructing]] {}

```jsx
const SidebarMenu = ({text, Icon}) => {

    return (

        <div>

            <Icon className='h-7'  />

            <span>{text}</span>

        </div>

     );

}

export default SidebarMenu;
```