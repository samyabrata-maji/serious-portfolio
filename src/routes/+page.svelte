<script>
  import '@src/app.css';
  import { MY_TECH_STACK } from '@data/project.data';
  import Project from '@components/project_section/Project.svelte';
  import TechStack from '@components/project_section/TechStack.svelte';
  import Footer from '@components/Footer.svelte';
</script>

<div>
  <div class="w-full p-32 flex flex-col gap-32">
    <div class="grid grid-rows-1 grid-cols-2 gap-8">
      <div>
        <h2 class="text-3xl font-bold pb-2">Too less or Too more?</h2>
        <p>
          Here's a list of my tech stack. These are technologies that I've worked with and have
          build some projects with. There are few more that I've tried but never built anything
          with. Those are not included. See my Github for my complete Tech Stack.
        </p>
      </div>
      <div class="flex flex-wrap justify-start h-fit gap-x-4">
        {#each MY_TECH_STACK as tech_stack}
          <TechStack icon={tech_stack.icon} title={tech_stack.title} />
        {/each}
      </div>
    </div>

    <Project />
  </div>

  <Footer />
</div>
