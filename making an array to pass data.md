```jsx
import { SparklesIcon } from "@heroicons/react/solid";

import Input from "./Input";

import Post from "./Post";

  

export default function Feed() {

  const post = [

    {

      id: '1',

      name: 'Raiden Snake',

      username: 'codewithraiden',

      userImg: 'https://oyster.ignimgs.com/mediawiki/apis.ign.com/metal-gear-rising-revengeance/e/e6/Raiden_Rising_Render.jpg',

      img: 'https://images.unsplash.com/photo-1441974231531-c6227db76b6e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80',

      text: 'nice view!',

      timestamp: '2h ago',

    },

    {

      id: '2',

      name: 'Raiden Snake',

      username: 'codewithraiden',

      userImg: 'https://oyster.ignimgs.com/mediawiki/apis.ign.com/metal-gear-rising-revengeance/e/e6/Raiden_Rising_Render.jpg',

      img: 'https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80',

      text: 'wowzers',

      timestamp: '2 days ago',

    }

  

  ]

  return (

    <div className="xl:ml-[370px] border-l border-r border-gray-200 xl:min-w-[576px] sm:ml-[73px] flex-grow max-w-xl ">

      <div className="flex py-2 px-3 sticky top-0 z-50 bg-white border-b border-gray-200 ">

        <h2 className="text-lg sm:text-xl font-bold cursor-pointer ">Home</h2>

        <div className="hoverEffect flex items-center justify-center ml-auto w-9 h-9">

          <SparklesIcon className="h-5" />

        </div>

      </div>

      <Input />

      {post.map((post)=>(

        <Post key={post.id} post={post}/>

      ))}

    </div>

  );

}
```

above has the data as a variable at the beginning of the component and then that get's passed to this snippet of code

```jsx
export default function Post({post}) {

  return (

    <div>{post.id}</div>

  )

}
```

