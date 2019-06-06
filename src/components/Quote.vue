<template>
    <div class="col-sn-6 col-md-4 col-lg-3">
        <div class="pannel pannel-default">
            <div class="pannel-body quote">
                <slot>

                </slot>
            </div>
        </div>
    </div>

</template>


<script>

</script>

<style>
    .pannel-body{
        font-family: 'Indie Flower', cursive;
        font-size: 24px;
        color : #6e6e6e;   
    }

    .quote {
        border: 2px black;
        cursor: pointer;
    }

    .quote:hover{
        background-color: #ffe2e2;
    }
</style>
