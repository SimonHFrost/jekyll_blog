---
layout: post
title: "Generating code from wireframes"
---

<style>
.post-content img {
  border: 1px solid black;
  box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.4);
  aspect-ratio: 16/9;
  height: auto;
  width: 100%;
  background-color: #f5f5f5;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  opacity: 1;
  transition: opacity 0.5s ease-in;
  color: transparent;
}

.post-content img:not(.loaded) {
  opacity: 0.8;
}

.post-content img.loaded {
  opacity: 1;
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function() {
  const images = document.querySelectorAll('.post-content img');

  images.forEach(function(img) {
    const src = img.src;
    const tempImg = new Image();

    // Set the background image immediately but keep it hidden
    img.style.backgroundImage = `url(${src})`;
    img.style.color = 'transparent';

    tempImg.onload = function() {
      img.classList.add('loaded');
    };

    tempImg.onerror = function() {
      img.classList.add('loaded');
    };

    tempImg.src = src;
  });
});
</script>

Converting wireframes automatically to code is easy right? With the press of the big ol' red AI button, you can transform static designs into well designed, interactive code. It is possible! But there are techniques you'll need to overcome to ensure you're faster than writing everything manually.

![Button](/assets/ai-code-generation/button.jpg)

## Building a solid foundation

AI performs better when it has context. Make sure you start with good boilerplate code and define important structural decisions so AI doesn't have to fill in the gaps.


#### Connect documentation

Clear documentation reduces hallucinations and means you'll waste less time explaining the same concepts through prompts, as well as minimise visual glitches or bugs.

In Cursor, you can link documentation URLs with the command @docs. Currently it's not clear how the documentation is indexed, you can also create local files and send them with requests. Transparency on how Cursor uses documentation to determine output is continuously improving...

![Documentation](/assets/ai-code-generation/documentation.jpg)

Ensure you add as much documentation as possible: component libraries, framework documentation, and local files like linting and code style.

#### Export designs

Designs are often static and don't accurately represent real-world variations in screen sizes and interactivity. But it's a good start!

If you're using Figma, I recommend the Figma to Code, or Builder.io export plugin, but find the best tool that works for you. Figma to Code is open source, so you can modify the generation if needed like adding custom html tags.

![Arrows](/assets/ai-code-generation/arrows.jpg)

Technology isn't quite there yet, so exported code won't be perfect. Take your time molding it to your needs and style, AI will be using it as an example frequently in the future!

## Chat it Out!

Generating a whole project or even separate screens can be difficult as there's much to interpret. It's time to leverage the 'Language' in Large Language Model (LLM), by breaking up the screens into conversations and chatting through your designs.

#### Keep Changes Small

Give AI less chance to get things wrong and use git commits as 'save points'. It's often faster to revert changes and try a different prompt, rather than debugging edge cases.

![Talking](/assets/ai-code-generation/talking.jpg)

It's time to level up your prompt engineering! Take time to be terse and provide references. Screenshots are amazing for inserting copy without even having to copy paste, they can also serve to communicate design terminology you might not know.

Mentioning existing components that the AI can use as a template is essential for making sure you have a consistent codebase.

#### Review Everything

Code may appear to be working at the surface, but dig a little and you'll find it often needs adjustments. Take care about code that's 'almost there'. If you rush forward, bugs will often compound while AI reference itself. It's better to catch problems early before they get out of control.

As always, having code quality tools like automated testing and linting are doubly as useful for AI.

When you commit your code it will ultimately be attributed to your identity. So if you don't read every single line generated, make sure you're happy to put your name behind it!

![Vibes](/assets/ai-code-generation/vibes.jpg)

Or you know… just vibe it out. It's your choice dude.

## Conclusion

AI is a perfect use case for generating code from wireframes, but it's far from being a one button-press solution.

For best results, start slowly to make sure that AI has high quality examples as you collaboratively chat it out. Keep changes small, and leverage existing tools like git for 'save points' and automated quality checks like linting to make sure your code base stays healthy.

Every day AI and humanity are learning from each other, let's continue exploring this relationship together...

![Sunset](/assets/ai-code-generation/sunset.jpg)