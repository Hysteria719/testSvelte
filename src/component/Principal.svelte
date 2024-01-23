<script lang="ts">
    export let bodyName: string = 'BodyParDefaut';
    import { onMount } from 'svelte'
    let component: any;

    onMount(async () => {
    
        try {
            /* @vite-ignore */
            const module = await import(`./${bodyName}.svelte`);
            component = module.default;
        }
        catch (e) {
            console.log("Erreur lors de l'importation du composant : ", e )
            component = null;
        }
    })
    
</script>

<svelte:component this={component} />
