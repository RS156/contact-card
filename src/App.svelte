<script>
  import avatar from "./assets/avatar.jpg";
  import Icon from "./lib/Icon.svelte";
  import "@fortawesome/fontawesome-free/css/all.css";
  import "@fortawesome/fontawesome-free/js/all.js";
  import "./app.css";
  import socialIconsInfo from "./assets/socialLinkIcons.json";
  import contactLinksInfo from "./assets/contactCardInfo.json";

  const socialIcons = socialIconsInfo;
  const contactLinks = contactLinksInfo;
</script>

<main>
  <div
    class="px-6 rounded-[20px] mx-4 md:mx-auto max-w-md mt-[180px] bg-gray-900 relative flex flex-col text-center mb-12 pb-4"
  >
    <img
      src={avatar}
      alt=""
      class="w-[200px] absolute left-[50%] transform -translate-x-[50%] h-[200px] drop-shadow-xl mx-auto rounded-[20px] -mt-[140px]"
    />
    <div
      class="mb-4 gap-2 relative text-center bg-gray-900 rounded-[50px] mt-[100px]"
    >
      <div class="">
        <h1 class="text-3xl font-semibold text-white">John Doe</h1>
        <h3
          class="mt-8 inline-block bg-gray-800 text-gray-400 px-6 py-3 rounded-lg text-lg"
        >
          UI/UX Designer
        </h3>
        <div class="mt-8 flex items-center justify-center gap-8">
          {#each socialIcons as sIcon (sIcon)}
            <Icon {...sIcon} />
          {/each}
        </div>
        <!-- contact area -->
        <div class="mt-8 bg-gray-800 px-4 py-4 rounded-lg">
          {#each contactLinks as contact, i (contact)}
            <div
              class="flex gap-4 items-center py-4 {i + 1 === contactLinks.length
                ? ''
                : 'border-gray-600 border-b'}"
            >
              <div class=""><Icon {...contact.icon} /></div>

              <div class="">
                <p class="text-left text-sm text-gray-400">{contact.label}</p>
                <p class="text-left text-base mt-1 break-all">{contact.info}</p>
              </div>
            </div>
          {/each}
        </div>
        <a
          href="/contact.vcf"
          download
          class="inline-flex items-center mx-auto bg-gradient-to-r from-[#FA5252] to-[#DD2476] duration-200 transition ease-linear hover:bg-gradient-to-r hover:from-[#DD2476] hover:to-[#FA5252] px-8 py-3 text-xl text-white rounded-[35px] mt-8"
          >Download Contact Card</a
        >
      </div>
    </div>
  </div>
</main>

<style lang="postcss">
</style>
