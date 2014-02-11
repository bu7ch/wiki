## RAILS ROUTEUR ##
Le routeur est une des parties centrale de l'application rails.<br>

La documentation du rails guide fait plusieurs distinctions.
<ul>
<li> </li>
</ul>

Rails routeur , connecte une url a du code, crée une url a partir du code et/ou genere une url.<br>

Le routeur Rails fonctionne de 3 manières<br>
Le fonctionnement par défaut par l'utilisation des resources (ndt Résolution des liens, controle des liens les thèmes ne sont pas fixés.).
Le fonctionnement par la non utilisation des resources.
La personnalisation des liens.

Des options pour inspecter et tester des routes seront abordés dans notre exemple.<br>>


La première optiion qui est celle par défaut dans rails est resources.
Ressources crée les liens index, new, edit , create, show, update et destroy. Elle est par défaut dans rails.

```
# resources :<NomController ou de plusieurs controller>
resources :photos
```

Imbrication et espace de noms, il s'agit du code suivant:

```

namespace :admin do
  resources :posts, :comments
end

```




Pour tout ce qui est ressources => ne jamais nicher de plus d'un niveau
L'alternative est d'utiliser les "shallow nesting"
