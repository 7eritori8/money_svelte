<script>
    let Yen = 0;

    const Dollar = 0.0074;
    const EUR = 0.007;
    const Yuan = 0.051;
    function getYen(e) {
        let value = e.target.value;
        if (value !== null && value >= 0) {
            Yen = value;
        }
    }
</script>

<h1>円→通貨計算機</h1>
<input on:input={getYen} type="number" min="0" maxlength="10" value="0" /><span
    >円</span
>
{#if Yen !== null}
    <h2>{Yen}円は・・・</h2>
    <p>{Dollar * Yen}ドル</p>
    <p>{EUR * Yen}ユーロ</p>
    <p>{Yuan * Yen}元</p>
{/if}
