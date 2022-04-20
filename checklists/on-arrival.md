<link href="../styles/custom.css" rel="stylesheet" />
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
    $(function(){
        $('.checklistToggler').each(function(i, el){
            var toggler = $(el);
            var togglerTarget = toggler.data('target');
            // initialise
            updateToggleState(toggler, false);  
            stripeChecklistItems();
            // click handler
            toggler.on('click', function(e){
                var isActive = !toggler.data('isActive');
                updateToggleState(toggler, isActive);  
                stripeChecklistItems();
                e.preventDefault();
            })
        });
        function updateToggleState(toggler, isActive) {
            toggler.data('isActive', isActive);
            var togglerTarget = toggler.data('target');
            if (isActive) {
                $('label.'+togglerTarget+'-Y').show();
                $('label.'+togglerTarget+'-N').hide();
                toggler.addClass('active');
            }
            else {
                $('label.'+togglerTarget+'-N').show();
                $('label.'+togglerTarget+'-Y').hide();
                toggler.removeClass('active');
            }
        }
        function stripeChecklistItems() {
            $('.checklistContainer label').removeClass('alt');
            $('.checklistContainer label:visible:odd').addClass('alt');
        }
    });
</script>

# On Arrival

Activate the site facilities available:

<ol class="togglelist">
    <li>
        <a href="#" title="Toggle 240v power" class="checklistToggler" data-target="power"><img src="x.png" alt="240v Power" /></a>
    </li>
    <li>
        <a href="#" title="Toggle mains water" class="checklistToggler" data-target="water"><img src="x.png" alt="Mains Water" /></a>
    </li>
    <li>
        <a href="#" title="Toggle greywater" class="checklistToggler" data-target="greywater"><img src="x.png" alt="Greywater" /></a>
    </li>
</ol>

## Checklist

<div class="checklistContainer">
<label><input type="checkbox" /> Select as flat and level a parking site as possible. Use leveling blocks if
required.</label>
<label class="power-Y"><input type="checkbox" /> Connect 240v electricity <br />
*Check if [15A to 10A Power Adaptor](../guides/power-adaptor.md) is required.*</label>
<label class="water-Y"><input type="checkbox" /> Connect city water </label>
<label class="greywater-Y"><input type="checkbox" /> Connect grey water </label>
<label><input type="checkbox" /> Ensure LPG gas bottle is open</label>
<label><input type="checkbox" /> Turn on button 1-3 on the [Battery and Water Control Panel](../guides/control-panel.md).</label>
<label class="water-N"><input type="checkbox" /> Turn the water pump on.<br/>
*Button 4 on the [Battery and Water Control Panel](../guides/control-panel.md)*
</label>
<label class="power-N"><input type="checkbox" /> Turn the hot water heater on using LPG gas.</label>
<label class="power-Y"><input type="checkbox" /> Turn the hot water heater on using 240v.</label>
<label class="power-N"><input type="checkbox" /> Ensure the refrigerator (in auto mode) is switched to LPG gas.</label>
<label class="power-Y"><input type="checkbox" /> Ensure the refrigerator (in auto mode) is switched to 240v.</label>
<label><input type="checkbox" /> If using LPG gas, turn the refrigerator fan on.</label>
</div>

> **Please note!** If using LPG gas, it can take up to **20 minutes** before the fridge turns on. 
>
> The refrigerator must be level and will not operate if not parked on a flat surface.

<a href="pre-departure.html"><button class="nav-button"><i class="arrow arrow-left"></i> Pre-Departure</button></a>
<a href="pre-return.html" class="right"><button class="nav-button">Pre-Return <i class="arrow arrow-right"></i></button></a>