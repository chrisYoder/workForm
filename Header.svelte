<script>
  const headerLinks = ["Self", "Someone Else"];
</script>

<ul>
  {#each headerLinks as link}
    <li class={link}>{link}</li>
  {/each}
</ul>

<style>
  ul {
    display: grid;
    grid-template-areas: "self else";
    grid-template-rows: 50px;
    grid-template-columns: 1fr 1fr;
    grid-gap: 1em;
    align-items: center;
  }
  li {
    list-style: none;
    border: 1px solid black;
  }

  .self {
    grid-area: self;
  }

  .someoneElse {
    grid-area: else;
  }
</style>