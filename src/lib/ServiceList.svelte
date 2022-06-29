<script>
    export let visible = false;
    export let map;
    import ServiceCard from "./ServiceCard.svelte";

    export function Display(tag)
    {
        visible = true;
    }

    export function Hide()
    {
        visible = false;
    }
</script>

<div id="services" class="columns col-oneline" style="display:{visible ? 'flex':'none'}">
    <button id="close" class="btn btn-link" on:click={() => Hide()}>
        <i class="icon icon-cross"></i>
    </button>
    <ServiceCard map={map}/>
    <ServiceCard map={map}/>
</div>

<style>
#services
{
    background: white;
    position: absolute;
    bottom: 0%;
    width: 100%;
    padding-bottom: 5%;
    padding-left: 5%;
    padding-top: 5%;
    margin-left: 3px;

    border-top-left-radius: 50px;
    border-top-right-radius: 50px;

    box-shadow: -2px -2px 42px 4px rgba(0,0,0,0.35);
    -webkit-box-shadow: -2px -2px 42px 4px rgba(0,0,0,0.35);
    -moz-box-shadow: -2px -2px 42px 4px rgba(0,0,0,0.35);
}
#close
{
    position: absolute;
    right: 30px;
    top: -4px;
}
</style>
