<script lang="ts">
  import { getCurrentWindow } from "@tauri-apps/api/window";

  let appWindow = getCurrentWindow()
</script>

<div data-tauri-drag-region style:height="35px" style:width="100%"></div>
<nav class="window-decoration">
    <button class="minimize-btn btn" on:click={() => appWindow.minimize()} title="minimize">
      <svg
        width="20"
        height="3"
        viewBox="0 0 20 3"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M1.66667 2.99998C1.19445 2.99998 0.798894 2.85598 0.480006 2.56798C0.161117 2.27998 0.00111686 1.92399 5.74712e-06 1.49999C-0.00110536 1.07599 0.158895 0.719995 0.480006 0.431997C0.801117 0.143999 1.19667 0 1.66667 0H18.3333C18.8056 0 19.2017 0.143999 19.5217 0.431997C19.8417 0.719995 20.0011 1.07599 20 1.49999C19.9989 1.92399 19.8389 2.28048 19.52 2.56948C19.2011 2.85848 18.8056 3.00198 18.3333 2.99998H1.66667Z"
          fill="currentColor"
        />
      </svg>
    </button>
    <button class="maximize-btn btn" on:click={() => appWindow.toggleMaximize()} title="toggle maximize">
      <svg
        width="23"
        height="20"
        viewBox="0 0 23 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M6.68056 1.125H3.34722C2.75785 1.125 2.19262 1.37083 1.77587 1.80842C1.35913 2.246 1.125 2.83949 1.125 3.45833V6.95833M21.125 6.95833V3.45833C21.125 2.83949 20.8909 2.246 20.4741 1.80842C20.0574 1.37083 19.4921 1.125 18.9028 1.125H15.5694M1.125 16.2917V19.7917C1.125 20.4105 1.35913 21.004 1.77587 21.4416C2.19262 21.8792 2.75785 22.125 3.34722 22.125H6.68056M15.5694 22.125H18.9028C19.4921 22.125 20.0574 21.8792 20.4741 21.4416C20.8909 21.004 21.125 20.4105 21.125 19.7917V16.2917"
          stroke="currentColor"
          stroke-width="2.25"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </button>
  <button class="close-btn btn" on:click={() => appWindow.close()} title="close">
    <svg
      width="20"
      height="20"
      viewBox="0 0 20 20"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M10 12.1293L2.54753 19.5817C2.26869 19.8606 1.91381 20 1.48289 20C1.05196 20 0.697084 19.8606 0.41825 19.5817C0.139416 19.3029 0 18.948 0 18.5171C0 18.0862 0.139416 17.7313 0.41825 17.4525L7.87072 10L0.41825 2.54753C0.139416 2.26869 0 1.91381 0 1.48289C0 1.05196 0.139416 0.697084 0.41825 0.41825C0.697084 0.139416 1.05196 0 1.48289 0C1.91381 0 2.26869 0.139416 2.54753 0.41825L10 7.87072L17.4525 0.41825C17.7313 0.139416 18.0862 0 18.5171 0C18.948 0 19.3029 0.139416 19.5817 0.41825C19.8606 0.697084 20 1.05196 20 1.48289C20 1.91381 19.8606 2.26869 19.5817 2.54753L12.1293 10L19.5817 17.4525C19.8606 17.7313 20 18.0862 20 18.5171C20 18.948 19.8606 19.3029 19.5817 19.5817C19.3029 19.8606 18.948 20 18.5171 20C18.0862 20 17.7313 19.8606 17.4525 19.5817L10 12.1293Z"
        fill="currentColor"
      />
    </svg>
  </button>
</nav>

<style lang="sass">

  .window-decoration
    display: flex
    background-color: #fff
    width: 100px
    height: 35px
    position: fixed
    top: 0
    right: 0
    justify-content: space-evenly
    align-items: center
    border-bottom-left-radius: 10px

  .btn
    border: none
    background-color: transparent
    transition: background-color .3s
    height: inherit
    width: 50px

  .minimize-btn
    border-bottom-left-radius: 10px

  .minimize-btn:hover, .maximize-btn:hover
    background-color: #ddd

  .close-btn:hover
    background-color: #ff0000
    color: #fff

</style>
