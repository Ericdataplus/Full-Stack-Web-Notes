with the sidebar we use subcomponents to help build it, [[SidebarMenu]], 

using [[heroicons]] for the same icons that the acual website uses quickly and free

```jsx
// heroicons

// import it into the component
import {HomeIcon} from "@heroicons/react/solid";

// apply it to a tag
<SidebarMenu text='Home' Icon={HomeIcon} />
```

Adding the icons as [[props]] to the [[SidebarMenu]] sub-component 

then we use the [[vs code shortcuts]] alt+shift+up/down arrow key to duplicate easily

```jsx
import {HomeIcon} from "@heroicons/react/solid";

<div className="">

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Home' Icon={HomeIcon} />

      </div>
```

then manually change to this 

```jsx
// import the corresponding packages
import {HomeIcon, BellIcon, HashtagIcon, BookmarkIcon, ClipboardIcon, DotsCircleHorizontalIcon, InboxIcon} from "@heroicons/react/solid";

<div className="">

        <SidebarMenu text='Home' Icon={HomeIcon} />

        <SidebarMenu text='Explore' Icon={HashtagIcon} />

        <SidebarMenu text='Notifications' Icon={BellIcon} />

        <SidebarMenu text='Messages' Icon={InboxIcon} />

        <SidebarMenu text='Bookmarks' Icon={BookmarkIcon} />

        <SidebarMenu text='Lists' Icon={ClipboardIcon} />

        <SidebarMenu text='More' Icon={DotsCircleHorizontalIcon} />

      </div>

```

after this we pretty much do a bunch of tailwind editing

```jsx
// side bar code will look like this

import Image from "next/image";

import SidebarMenu from "./SidebarMenu";

import {

  BellIcon,

  HashtagIcon,

  BookmarkIcon,

  ClipboardIcon,

  DotsCircleHorizontalIcon,

  HomeIcon,

  InboxIcon,

  DotsHorizontalIcon,

} from "@heroicons/react/solid";

  

const Sidebar = () => {

  return (

    <div className="hidden sm:flex flex-col p-2 xl:items-start fixed h-full">

      {/* Twitter Logo */}

      <div className="hoverEffect p-0 hover:bg-blue-100 xl:px-1">

        <Image

          width="50"

          height="50"

          src="https://help.twitter.com/content/dam/help-twitter/brand/logo.png"

        ></Image>

      </div>

  

      {/* Menu */}

  

      <div className="mt-4 mb-2.5 xl:items-start">

        <SidebarMenu text="Home" Icon={HomeIcon} active />

        <SidebarMenu text="Explore" Icon={HashtagIcon} />

        <SidebarMenu text="Notifications" Icon={BellIcon} />

        <SidebarMenu text="Messages" Icon={InboxIcon} />

        <SidebarMenu text="Bookmarks" Icon={BookmarkIcon} />

        <SidebarMenu text="Lists" Icon={ClipboardIcon} />

        <SidebarMenu text="More" Icon={DotsCircleHorizontalIcon} />

      </div>

  

      {/* Button */}

  

      <button className="bg-blue-400 text-white rounded-full w-56 h-12 font-bold shadow-md hover:brightness-95 text-lg hidden xl:inline">

        Tweet

      </button>

  

      {/* Mini-Profile */}

  

      <div className="hoverEffect text-gray-700 flex items-center justify-center xl:justify-start mt-auto ">

        <img

          src="https://oyster.ignimgs.com/mediawiki/apis.ign.com/metal-gear-rising-revengeance/e/e6/Raiden_Rising_Render.jpg"

          alt="user-img"

          className="h-10 w-10 rounded-full xl:mr-2"

        />

        <div className="leading-5 hidden xl:inline">

          <h4 className="font-bold">Raiden Solid</h4>

          <p className="text-gray-500">@RaidenSolidMercs</p>

        </div>

        <DotsHorizontalIcon className="h-5 xl:ml-8 hidden xl:inline" />

      </div>

    </div>

  );

};

  

export default Sidebar;

```

and

```jsx
// SidebarMenu Subcomponent will look like this

const SidebarMenu = ({ text, Icon, active }) => {

  return (

    <div className="hoverEffect flex items-center text-gray-400 justify-center xl:justify-start text-lg space-x-3">

      <Icon className="h-7" />

      <span className={`${active && "font-bold"} hidden xl:inline`}>

        {text}

      </span>

    </div>

  );

};

  

export default SidebarMenu;

```

with the above so far and with the SidebarMenu Subcomponent site should look like this and we are done for now with the sidebar and made the hypothetical git add . , git commit -m 'message goes here' and git push 

![[Screenshot 2022-07-12 181107.png]]






