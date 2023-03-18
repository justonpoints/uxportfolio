<script lang='ts'>
    import Fa from 'svelte-fa/src/fa.svelte'
    import {faCompassDrafting,faShareNodes, faGraduationCap, faArrowUpRightFromSquare, faBriefcase, faUserNinja } from '@fortawesome/free-solid-svg-icons'

    export let category;
    export let title;
    export let date;
    export let path;

    let catIcon:any;
    let catName;
    let catLink

    setCat(category);


    function setCat(cat){
        switch(cat){
            case "education":
                catIcon = faGraduationCap;
                catName = "Education";
                catLink = "/education";
                break;
            case "experience":
                catIcon = faBriefcase;
                catName = "Experience";
                catLink = "/experience";
                break;
            case "skills":
                catIcon = faUserNinja;
                catName = "Skills";
                catLink = "/skills";
                break;
            case "social":
                catIcon = faShareNodes;
                catName = "Social";
                catLink = "/social";
                break;
            case "design":
                catIcon = faCompassDrafting;
                catName = "Design";
                catLink = "/designs";
                break;
            default:
                return faArrowUpRightFromSquare
        }
    }

    function setCatUrl(){

    }

</script>

<article class="w-full flex flex-col flex-stretch shadow-2xl mt-5 mb-5 bg-white text-black min-h-fit">
    <div class="bg-black h-52 md:text-2xl w-full flex flex-col p-5">
        <div class="flex flex-col items-start justify-items-start">
                <a class="block text-white" href="{catLink}">
                        {catName}
                        <Fa class="inline" icon={faArrowUpRightFromSquare} />
                </a>
        </div>
        <div class="m-auto w-full flex items-center justify-items-center flex-col">
            <div class="block m-auto text-white">
                    <Fa class="text-8xl" icon={catIcon} />
            </div>
        </div>
    </div>
    <header class="text-center p-5">
        <h2 class="text-2xl">{title}<h2>
        <div class="text-lg">{date}</div>
    </header>
    <div class="p-5">
        <slot/>
        <a class="border-black border block p-2 mt-5 float-right md:text-xl" href="/article">Go to Article</a>
    </div>
</article>


<style>
</style>
