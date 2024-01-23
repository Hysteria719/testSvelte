<script>
// @ts-nocheck

    import Sidebar from '../component/Sidebar.svelte'
    import TopBar from '../component/TopBar.svelte'
    import Body from '../component/Body.svelte'
    import Footer from '../component/Footer.svelte'
    import Principal from '../component/Principal.svelte';

    let sidebarItems = [
        {id: 1, label: 'Accueuil'},
        {id: 2, label: 'Profil'},
        {id: 3, label: 'Pramètre'},               
    ];

</script>

<div class="SideBar">
    <Sidebar items={sidebarItems} />
    <div class="div2">
        <TopBar/>        
        <Body>
            <h2>Bienvenue dans mon application</h2>    
            <p>Ceci est le corps de la page.</p>
            <Principal/>
            <Principal bodyName="BodyA"/>
        </Body>
        <Footer />
    </div>

</div>

<style>
    .SideBar {
        display: flex;
        height:100vh;
    }

</style>


