---
layout: home
---

{% if site.theme_config.show_projects == true %}

<h2>{{ site.theme_config.home.title_projects }}</h2>

  {% include card_list.html collection=site.data.home.project_entries %}

{% endif %}

{% if site.theme_config.show_misc_list == true %}

<h2>{{ site.theme_config.home.title_misc_list }}</h2>

  {% include vertical_list.html collection=site.data.home.misc_entries %}

{% endif %}

{% if site.theme_config.show_blog == true %}

<h2>{{ site.theme_config.home.title_blog }}</h2>

  {% include post_list.html %}

{% endif %}

{% if site.theme_config.show_old_projects == true %}

<h2>{{ site.theme_config.home.title_old_projects }}</h2>

  {% include card_list.html collection=site.data.home.old_project_entries %}

{% endif %}

<script>
document.addEventListener('DOMContentLoaded', function () {
    const customCursor = document.createElement('div');
    customCursor.className = 'custom-cursor';
    document.body.appendChild(customCursor);

    document.body.addEventListener('mousemove', (e) => {
        customCursor.style.left = e.clientX + 'px';
        customCursor.style.top = e.clientY + 'px';
    });

    // Add a hover effect to the moonlight table
    const moonlightTable = document.querySelector('.moonlight-table');
    moonlightTable.addEventListener('mouseenter', () => {
        customCursor.style.width = '40px';
        customCursor.style.height = '40px';
    });

    moonlightTable.addEventListener('mouseleave', () => {
        customCursor.style.width = '20px';
        customCursor.style.height = '20px';
    });
});
</script>
