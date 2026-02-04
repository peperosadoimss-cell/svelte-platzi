<script>
    let skills = [
        { id:1,  name: 'JavaScript', level: 'Advanced' },
        { id:2, name: 'Svelte', level: 'Intermediate' },
        { id:3, name: 'CSS', level: 'Advanced' },
        { id:4, name: 'HTML', level: 'Advanced' },
        { id:5, name: 'TypeScript', level: 'Intermediate' }
    ];
</script>
<style>
    .Skills {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
    }
    li{
        display: inline;
        margin: 0 0 0 0.4em;
    }

</style>

<div class="Skills">
    <h3>Habilidades: </h3>
    <ul>
        {#each skills as {name}, i}
            <li>{name}</li>
        {/each}
    </ul>
<!--    {#each skills as skill}
        <div class="skill" id={"skill-" + skill.id}>
            <h3>{skill.name}</h3>
            <p>Level: {skill.level}</p>
        </div>
    {/each} -->
</div>