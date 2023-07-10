<script>
    import "@fortawesome/fontawesome-free/css/all.css";
    import "@fortawesome/fontawesome-free/js/all.js";
    import "../app.css";

    export let bgColor;
    export let iconColor;
    export let iconClass;
    export let siteLink = "none";
</script>

{#if siteLink === "none"}
    <span
        class="w-12 h-12 flex items-center justify-center rounded-lg
    hover:bg-gradient-to-r hover:from-[#fa5252] hover:to-[#dd2476] hover:text-white
    duration-200 transition ease-linear {bgColor} {iconColor}"
    >
        <i class={iconClass} />
    </span>
{:else}
    <a
        href="https://www.facebook.com/"
        target="_blank"
        rel="noopener noreferrer"
        ><span
            class="w-12 h-12 flex items-center justify-center rounded-lg
    cursor-pointer hover:bg-gradient-to-r hover:from-[#fa5252] hover:to-[#dd2476] hover:text-white
    duration-200 transition ease-linear text-lg {bgColor} {iconColor}"
        >
            <i class={iconClass} />
        </span>
    </a>
{/if}
