<script>
    export let map;
    export let service = {
        image: "https://picturepan2.github.io/spectre/img/osx-yosemite-2.jpg",
        name: "Demo Service",
        type: "Bathroom",
        lat: 17.4482809,
        long: 78.3487633
    };
</script>

<div class="column col-10 card p-0 m-2">
    <div class="card-image" style="height: 75px;">
        <div class="image" style="background: url({service.image})"> </div>
    </div>
    <div class="card-header">
        <button class="btn btn-primary float-right" on:click={() => map.focus(service.long, service.lat)}>
            <i class="icon icon-location"></i>
        </button>
        <div class="card-title h5">{service.name}</div>
        <div class="card-subtitle text-gray">{service.type}</div>
    </div>
    <div class="card-footer">
        <button class="btn btn-primary">
            Know More
        </button>
    </div>
</div>

<style>
.image
{
    background-size: cover;
    height: 100%;
    overflow-y: hidden;
}
</style>
