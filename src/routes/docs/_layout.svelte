<script lang="ts">
    export let segment: string;
</script>

<style>
/* #f19066 */
    .sidenav {
        height: 100%;
        width: 160px;
        position: absolute;
        z-index: 1;
        top: 0;
        left: 0;
        background-color: #f1f2f6;
        overflow-x: hidden;
        margin-top: 20px;
    }

    .sidenav a {
        padding: 6px 8px 6px 16px;
        text-decoration: none;
        font-size: 12px;
        color: #000;
        display: block;
    }
    .sidenav a:hover, .sidenav a[aria-current] {
        background-color: #f19066;
    }

    .main {
        margin-left: 160px; /* Same as the width of the sidenav */
        padding: 0px 10px;
    }

    @media screen and (max-height: 450px) {
        .sidenav {
            padding-top: 15px;
        }
        .sidenav a {
            font-size: 18px;
        }
    }
</style>

<div class="sidenav">
    <a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Foreword</a>
    <a aria-current="{segment === 'introduction' ? 'page' : undefined}" href="introduction">Introduction</a>
    <a aria-current="{segment === 'setup' ? 'page' : undefined}" href="setup">Setup</a>
</div>
<main class="main">
    <slot />
</main>
