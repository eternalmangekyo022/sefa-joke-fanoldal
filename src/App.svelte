<script lang="ts">
  let hovering = false;
  const instagram = 'https://www.instagram.com/zolikomuves_/';
  const tiktok = 'https://www.tiktok.com/@komuves.zoli_?lang=en';
  const twitter = 'https://twitter.com/komuves_zoli';
  const youtube = 'https://www.youtube.com/c/ZoliKomuves/videos';

  $: iconWidth = 50;
</script>

<div class="h-full w-full relative">
  <div
    class="w-[70%] max-w-3xl h-full absolute left-1/2 -translate-x-1/2 bg-[#ceecb4] flex flex-col items-center"
  >
    <header class="w-full flex flex-col justify-center items-center">
      <h4 class="font-bold my-10">sziasztok sefa vagyok</h4>
      <div
        class="aspect-square bg-black relative"
        style={`width: ${window.innerWidth * 0.6}px; max-width: 30rem;`}
        on:mouseenter={() => {
          hovering = true;
        }}
        on:mouseleave={() => {
          hovering = false;
        }}
      >
        <img
          class="absolute"
          draggable="false"
          src="https://yt3.ggpht.com/tKGoIFNLbtGjSBQBGGPqYfu8D3uIydk0TM-q1PoIv15kg2qG7nCTiiIMIcPo01WcEAXoKER3=s900-c-k-c0x00ffffff-no-rj"
          alt="sefa"
          width={window.innerWidth * 0.6}
        />
        <div
          style={`visibility: ${
            hovering ? 'visible' : 'hidden'
          }; background-color: ${hovering ? 'rgba(87, 86, 86, .5)' : 'none'};`}
          class={`absolute ${
            hovering && 'bg-[rgba(87, 86, 86, 1)]'
          } w-full h-full flex flex-col justify-around items-center`}
        >
          <!-- svelte-ignore a11y-click-events-have-key-events -->
          <img
            width={iconWidth}
            class="cursor-pointer"
            src="https://www.svgrepo.com/show/28730/youtube.svg"
            alt="Twitter"
            on:click={() => window.open(youtube)}
          />
          <!-- svelte-ignore a11y-click-events-have-key-events -->
          <img
            src="https://www.svgrepo.com/show/157806/instagram.svg"
            alt="Instagram"
            class="cursor-pointer"
            width={iconWidth}
            on:click={() => window.open(instagram)}
          />
          <!-- svelte-ignore a11y-click-events-have-key-events -->
          <img
            width={iconWidth}
            class="cursor-pointer"
            src="https://www.svgrepo.com/show/342294/tiktok.svg"
            alt="TikTok"
            on:click={() => window.open(tiktok)}
          />
          <!-- svelte-ignore a11y-click-events-have-key-events -->
          <img
            width={iconWidth}
            class="cursor-pointer"
            src="https://www.svgrepo.com/show/183608/twitter.svg"
            alt="Twitter"
            on:click={() => window.open(twitter)}
          />
        </div>
      </div>
    </header>
    <span>Hobbim a gitározás</span>
  </div>
</div>
