<script>
    let signup = "signe"
    let register = "enregistre"
    let main = "principal"
    export let test = "defaut";
    console.log("test : ", test)
    
    const component = {
        Signup: test,
        Register: register,
        Main : main,
    }
    console.log("component 1 : ", component['Signup'])
</script>

<div>{component['Signup']}</div>