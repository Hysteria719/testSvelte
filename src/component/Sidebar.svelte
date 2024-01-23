<script lang="ts">
    export let items: any;
</script>

<aside>
    <ul>
        {#each items as item (item.id)}
        <li>{item.label}</li>
        {/each}
    </ul>
</aside>

<style>
    aside {
        width: 200px;
        background-color: #f0f0f0;
        padding: 10px;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    li {
        margin-bottom: 5px;
    }

</style>