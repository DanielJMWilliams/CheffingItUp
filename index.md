---
layout: default
title: "Paulina Eats"
---

<div class="container mx-auto">
  <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    {% for recipe in site.recipes %}
      <div class="bg-white rounded-lg shadow-md overflow-hidden">
        <a href="{{ recipe.url | relative_url}}">
          <img class="w-full h-48 object-cover" src="{{ recipe.image | relative_url }}" alt="{{ recipe.title }}">
        </a>
        <a href="{{ recipe.url | relative_url}}">
        <div class="p-4">
          <h2 class="text-xl font-semibold mb-2">{{ recipe.title }}</h2>
          <p class="text-gray-600">{{ recipe.description }}</p>
        </div>
        </a>
      </div>
    {% endfor %}
  </div>
</div>


