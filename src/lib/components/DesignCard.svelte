<script>

export let img;
export let title;
export let desc;

</script>

<div class="p-5 m-5 bg-white shadow-lg w-full">
  <div class="card-image">
    <figure class="h-fit">
      <img src="{img}" alt="{title}">
    </figure>
  </div>
  <div class="card-content">
    <div class="media">
      <div class="media-content">
        <p class="title is-4">{title}</p>
      </div>
    </div>

    <div class="content">
      {desc}
    </div>

  </div>
</div>


<style>
    .title{
        text-align:center;
        font-size: 18px;
        line-height: unset;
    }

    .card{
        width: 350px;
        margin: auto;
    }

</style>