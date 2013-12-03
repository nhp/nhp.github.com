---
layout: post
title: "Configurable Products with Tier prices"
description: ""
category: magento
tags: []
---
{% include JB/setup %}
In magento i missed a very cruical feature: product spanning tier prices. At least for within configurable products Simon Sprankel developed an extension a while ago.

Sadly we got into a rewrite conflict with DerModPros Better Configurabe Products because both extensions try to rewrite Mage_Catalog_Model_Product_Type_Configurable_Price. I really needed the functionality of bcp to use the prices of the simple products instead of option-based price correction and so i decided to join both extensions to have the best from both worlds.

The easiest part was to integrate Simons code into bcp by simply adding Helper/Admin.php and adding his functions to DerModPro_BCP_Model_Catalog_Prodcut_Type_Configurable_Price.
Then it became somewhat problematic because bcp uses the price defined by the simple product you are really putting in the cart instead of the configurables. 

I will enhance this post with a patch for bcp after i get the ok from the bcp-maintainers.
