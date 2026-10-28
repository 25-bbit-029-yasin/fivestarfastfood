Five Star Website v116 — order scrolling fix

Fixes: recalculates the order-list scroll state after the Admin Orders tab becomes visible, after switching between Staff Orders and Settings, when the order data is unchanged, and on viewport resize. Uses matching scroll thresholds for CSS max-heights. The page/document retains normal scrolling, while long order lists scroll independently and allow scroll chaining at their boundaries.

Checks: JavaScript syntax and ZIP integrity checks are run during packaging. Full live browser testing against a running server has not been performed.
