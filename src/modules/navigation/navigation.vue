<template>
  <header
    class="bg-neutral-950 grid grid-cols-3 border-b-4 border-b-neutral-700 justify-between items-center p-3"
  >
    <div>
      <button
        class="hover:bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
      >
        <img
          src="/icons/spotify_logo.png"
          width="32"
          height="32"
          alt="Spotify Logo"
        />
      </button>
    </div>
    <div class="gap-2 flex">
      <button
        class="bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer hover:scale-110"
      >
        <img
          src="/icons/navigation/home.png"
          width="32"
          height="32"
          alt="Spotify Logo"
        />
      </button>
      <form
        class="flex gap-2 hover:bg-neutral-800 bg-neutral-800 rounded-full px-2 w-full"
        action=""
      >
        <button
          class="p-2 rounded-full hover:scale-105 transition-all duration-75 cursor-pointer"
        >
          <img
            src="/icons/navigation/search.png"
            width="24"
            height="24"
            alt="Profile picture"
          />
        </button>
        <input
          type="search"
          placeholder="Search"
          class="bg-transparent w-full text-neutral-100 focus:outline-none"
        />
      </form>
      <button
        class="bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer hover:scale-110"
      >
        <img
          src="/icons/navigation/explore.png"
          width="32"
          height="32"
          alt="Spotify Logo"
        />
      </button>
    </div>
    <div class="flex justify-end">
      <button
        class="hover:bg-neutral-800 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
      >
        <img
          src="/icons/navigation/profile.png"
          width="24"
          height="24"
          alt="Profile picture"
        />
      </button>
    </div>
  </header>
</template>
