<script context="module">
    import {stories} from "./_stories";
    export async function preload({ params, query }) {
        let story = stories.find(s => s.slug === params.slug);
        if (story)
            return { story };
        else
            this.error(404, "Нет такой истории");
    }
</script>

<script>
    export let story;
    let title = story.title;
    let clauses = story.clauses.slice()
            .map(c => {
                return {
                    order: Math.random(),
                    clause: c
                }
            }).
            sort((a, b) => a.order - b.order);

    let index = -1;
    let text = "";

    function start(){
        index = 0;
        text = clauses[index].clause;
    }

    function next(){
        if (index < clauses.length - 1)
        {
            index++;
            text = clauses[index].clause;
        }
    }
</script>

{#if index===-1}
    <h2>{title}</h2>
    <button on:click={start}>Start</button>
{:else}
    <h3>{text}</h3>
    <button on:click={next}>next</button>
{/if}
