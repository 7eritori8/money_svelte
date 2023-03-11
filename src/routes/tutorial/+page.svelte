<script>
    console.log("aaa");
    let name = "eri";
    let src = "https://placehold.jp/150x150.png";
    import Child from "./child.svelte";
    let count = 0;
    function plusCount() {
        count = count + 1;
    }
</script>

<h1>Welcome to SvelteKit</h1>
<p>
    Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation
</p>
<p>{name}</p>
<input type="text" />

<!-- 画像 -->
<img {src} alt="" srcset="" />
<!-- 変数名と属性名が同じならこれでもOK -->
<img {src} alt="" srcset="" />

<!-- 別コンポーネントをインポート、表示 -->
<Child />

<button on:click={plusCount}> ぷっしゅ </button>
<span>{count}</span>

<!-- 別ページを作るときは、routesディレクトリ直下に作りたいパス名のフォルダを作成 -->
<!-- 作成したフォルダの中に+page.svelteファイルを作ると表示される -->

<!-- routesディレクトリ直下はホーム -->
<style>
    p {
        color: red;
    }
</style>
