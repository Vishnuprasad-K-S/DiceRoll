<h1>Dice Roll</h1>

<div class="image-container">
    <img src="{img}" alt="">
</div>

<div class="button-container">
    <button on:click={rollDice}>Roll Dice</button>
</div>

<style>
    h1 {
        font-family: Arial, Helvetica, sans-serif;
        text-align: center;
    }

    .button-container {
        margin-top: 20px;
        display: flex;
        justify-content: center;
    }

    .image-container {
        display: flex;
        justify-content: center;
    }

    button {
        background-color: white;
        border: 1px solid cyan;
        border-radius: 8px;
        font-size: 20pt;
        font-weight: 700;
        width: 300px;
        height: 60px;
    }
</style>

<script>
    import dice_1 from "$lib/assets/Dice_1.png";
    import dice_2 from "$lib/assets/Dice_2.png";
    import dice_3 from "$lib/assets/Dice_3.png";
    import dice_4 from "$lib/assets/Dice_4.png";
    import dice_5 from "$lib/assets/Dice_5.png";
    import dice_6 from "$lib/assets/Dice_6.png";
    const faces = [1,2,3,4,5,6];
    var random = 0;
    var img = '';

    function rollDice() {
        random = Math.floor(Math.random() * faces.length);
        console.log(random)

        switch (faces[random]) {
            case 1:
                img = dice_1;
                break;

            case 2:
                img = dice_2;
                break;

            case 3:
                img = dice_3;
                break;

            case 4:
                img = dice_4;
                break;

            case 5:
                img = dice_5;
                break;

            case 6:
                img = dice_6;
                break;

            default:
                break;
        }
    }

</script>
