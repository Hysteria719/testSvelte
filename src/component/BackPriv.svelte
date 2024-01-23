<script context="module" lang="ts"> 
    export let bodyName: string = 'BodyParDefaut';

    async function getComponent() {
        try {
            /* @vite-ignore */
            const module = await import(`./${bodyName}.svelte`);
            return module.default;
        }
        catch (e) {
            console.log("Erreur lors de l'importation du composant : ", e )
            return null;
        }
    }
</script>

<script lang="ts">
    import { onMount } from 'svelte'
    let Component: any;
    onMount(async () => {
        Component = await getComponent();
    });
</script>
<svelte:component this={Component} />
