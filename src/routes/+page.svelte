<script lang="ts">
    import { onMount } from 'svelte';
    import { base } from '$app/paths';

    const images = import.meta.glob("/src/lib/src_imgs/*", { eager: true, query: "?url", import: "default" });
    const srcImgs: string[] = Object.values(images) as string[];

    onMount(() => {
        if (window.location.hash === '#src-imgs') {
            document.getElementById('src-imgs')?.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }
    });
</script>

<h1>How I made "Crackly"</h1>
<p class="page-link"><a href="{base}/#src-imgs">See source images</a> <a href="{base}/font">Get the font</a> </p>


<div class="main-container">
    <div class="main-content">
        <h2>Why?</h2>
        <p>Hack Club announced the YSWS <a href="https://typeface.hackclub.com/">Typeface</a> 
            and I got the idea to take photos on my trip to Thailand and make a font by using 
            a bunch of diffrent letters from diffrent stuff.</p>

        <hr>

        <h2>How?</h2>
        <p>
            I took photos on my way to and in Thailand. 
            Then I cut them out, made them B&W and added them to a 
            <a href="https://www.calligraphr.com/">Calligraphr</a> template in Affinity.
        </p>

        <strong>That process looked something like this:</strong>
            <ol>
                <li>
                    <p>Take a photo.</p>
                    <img src="{base}/how_images/step1.webp" alt="1" class="how-img">
                </li>
                <li>
                    <p>Cut it out.</p>
                    <img src="{base}/how_images/step2.webp" alt="1" class="how-img">
                </li>
                <li>
                    <p>Apply ajustment layers to make it all black.</p>
                    <img src="{base}/how_images/step3.webp" alt="1" class="how-img">
                </li>
                <li>
                    <p>Add to corresponding spot in Calligraphr template.</p>
                    <img src="{base}/how_images/step4.webp" alt="1" class="how-img">
                </li>
                <li>
                    <em>When that has been done for all charachters. Upload to Calligraphr.</em>
                </li>
            </ol>

        <hr>

        <h2 id="src-imgs">Source images <em>(Unorderd)</em></h2>
        
        <div class="src-imgs-container">
            {#each srcImgs as img}
                <img src={img} alt="Char" class="src-img">
            {/each}
        </div>

        <hr class="bottom-hr">
        <em>
            The font "Crackly" and all associated source images are licenced under <a href="//creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a>
            , An <a href="https://github.com/Trulle1234/font-website/blob/main/LICENCE">MIT licence</a> applies to all else.
        </em>
    </div>
</div>