# Personalizar-menu-Wordpress

```
<?php $resdes = wp_get_nav_menu_items('redes-sociales'); ?>

<?php if (count($resdes) > 0): ?>
	<div class="ecr-redes pull-right">
		<ul>
			<?php foreach ($resdes as $key): ?>
				<?php if ($key->post_status == 'publish'): ?>
					<li>
            <a href="<?=$key->url?>" rel="no-fallow" class="hvr-grow">
              <i class="fa <?=getIconFont($key->post_title)?>" aria-hidden="true"></i>
            </a>
          </li>
				<?php endif ?>
			<?php endforeach ?>
		</ul>
	</div>
<?php endif ?>
```
