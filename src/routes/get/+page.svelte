<script lang="ts">
    import { asset, resolve } from '$app/paths';
</script>

<h1>Get Crackly</h1>
<p class="page-link"><a href={resolve("/")}>Go back</a></p>

<div class="main-container">
    <div class="font-content">
        <p class="font-preview">! ? : / " , . 0 1 2 3 4 5 6 7 8 9</p>
        <p class="font-preview">A B C D E F G H I J K L M N O P Q R S T U V W X Y Z Å Ä Ö</p>
        <p class="font-preview">a b c d e f g h i j k l m n o p q r s t u v w x y z å ä ö</p>
        <p class="font-preview">The quick brown fox jumps over the lazy dog.</p>

        <a href={asset("/Crackly-sans&serif.ttf")} download="Crackly-sans&serif.ttf" class="download">Download it</a>
        <hr class="bottom-hr">
        <em>
            The font "Crackly" and all associated source images are licenced under <a href="//creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a>
            , An <a href="https://github.com/Trulle1234/Crackly/blob/main/LICENCE.md">MIT licence</a> applies to all else.
        </em>
    </div>
</div>
