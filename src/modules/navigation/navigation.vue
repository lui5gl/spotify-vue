<template>
  <header
    class="bg-neutral-950 grid grid-cols-3 justify-between items-center p-3"
  >
    <section>
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
    </section>
    <section class="gap-3 flex">
      <button
        class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
      >
        <img
          src="/icons/navigation/home.png"
          width="32"
          height="32"
          alt="Spotify Logo"
        />
      </button>
      <form
        class="flex gap-2 hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 bg-neutral-800 rounded-full px-2 w-full focus:ring-4 focus:ring-neutral-100/25"
        action=""
      >
        <button
          class="hover:bg-neutral-800 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
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
        class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
      >
        <img
          src="/icons/navigation/explore.png"
          width="32"
          height="32"
          alt="Spotify Logo"
        />
      </button>
    </section>
    <section class="flex justify-end">
      <button
        class="hover:bg-neutral-800 hover:ring-4 ring-neutral-100/25 hover:scale-105 bg-neutral-800 p-2 rounded-full transition-all duration-75 cursor-pointer"
      >
        <img
          src="/icons/navigation/profile.png"
          width="24"
          height="24"
          alt="Profile picture"
        />
      </button>
    </section>
  </header>
</template>
