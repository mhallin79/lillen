---
title: On Arrival &#8729; Checklists 
---

<link href="../styles/custom.css" rel="stylesheet" />
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.6.1/dist/css/bootstrap.min.css" integrity="sha384-zCbKRCUGaJDkqS1kPbPd7TveP5iyJE0EjAuZQTgFLD2ylzuqKfdKlfG/eSrtxUkn" crossorigin="anonymous">
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
This checklists is also available in a [PDF version](/docs/checklists.pdf) for offline use.

Activate the site facilities available:

<ol class="togglelist">
    <li>
        <a href="#" title="Toggle 240V power" class="checklistToggler" data-target="power"><img src="images/power.png" alt="240V Power" /></a>
    </li>
    <li>
        <a href="#" title="Toggle mains water" class="checklistToggler" data-target="water"><img src="images/water.png" alt="Mains Water" /></a>
    </li>
    <li>
        <a href="#" title="Toggle greywater" class="checklistToggler" data-target="greywater"><img src="images/greywater.png" alt="Greywater" /></a>
    </li>
</ol>

## Checklist

<div class="checklistContainer">
<label><input type="checkbox" /> Select as flat and level a parking site as possible. Use leveling blocks if
required.</label>
<label class="power-N"><input type="checkbox" />Ensure the solar panels are not covered by shade as then they 
will not charge the 12V battery properly.</label>
<label class="power-Y"><input type="checkbox" /> Connect 240V electricity <br />
<em>Check if <a href="../guides/hoses-and-cables.html">15A to 10A Power Adaptor</a> is required.</em></label>
<label class="water-Y"><input type="checkbox" /> Connect to city water </label>
<label class="greywater-Y"><input type="checkbox" /> Connect greywater </label>
<label><input type="checkbox" /> Ensure LPG gas bottle is open</label>
<label><input type="checkbox" /> Turn on button 1-3 on the <a href="../guides/control-panel.html">Battery and Water Control Panel</a>.</label>
<label class="water-N"><input type="checkbox" /> Turn the water pump on.<br/>
<em>Button 4 on the <a href="../guides/control-panel.html">Battery and Water Control Panel</a></em>
</label>
<label class="power-N"><input type="checkbox" /> Turn the hot water heater on using the Gas button.<br />
<em>The <a href="hot-water-system.md">Hot Water Heater Controls</a> are located on the left-hand side back lounge area</em></label>
<label class="power-Y"><input type="checkbox" /> Turn the hot water heater on using the Electric button.<br />
<em>The <a href="hot-water-system.md">Hot Water Heater Controls</a> are located on the left-hand side back lounge area</em></label>
<label class="power-N"><input type="checkbox" /> Ensure the refrigerator (in auto mode) is switched to LPG gas.</label>
<label class="power-Y"><input type="checkbox" /> Ensure the refrigerator (in auto mode) is switched to 240V.</label>
<label class="power-N"><input type="checkbox" /> Ensure the refrigerator fan is switched on.</label>
</div>

<div class="alert alert-info">
    <svg class="svg-inline--fa fa-info-circle fa-w-16" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="info-circle" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" data-fa-i2svg=""><path fill="currentColor" d="M256 8C119.043 8 8 119.083 8 256c0 136.997 111.043 248 248 248s248-111.003 248-248C504 119.083 392.957 8 256 8zm0 110c23.196 0 42 18.804 42 42s-18.804 42-42 42-42-18.804-42-42 18.804-42 42-42zm56 254c0 6.627-5.373 12-12 12h-88c-6.627 0-12-5.373-12-12v-24c0-6.627 5.373-12 12-12h12v-64h-12c-6.627 0-12-5.373-12-12v-24c0-6.627 5.373-12 12-12h64c6.627 0 12 5.373 12 12v100h12c6.627 0 12 5.373 12 12v24z"></path></svg>
    <strong>Info:</strong> If using LPG gas, it can take up to <b>20 minutes</b> before the fridge turns on. 
</div>

<div class="alert alert-warning">
    <svg class="svg-inline--fa fa-triangle-exclamation fa-w-16" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="triangle-exclamation" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path fill="currentColor" d="M506.3 417l-213.3-364c-16.33-28-57.54-28-73.98 0l-213.2 364C-10.59 444.9 9.849 480 42.74 480h426.6C502.1 480 522.6 445 506.3 417zM232 168c0-13.25 10.75-24 24-24S280 154.8 280 168v128c0 13.25-10.75 24-23.1 24S232 309.3 232 296V168zM256 416c-17.36 0-31.44-14.08-31.44-31.44c0-17.36 14.07-31.44 31.44-31.44s31.44 14.08 31.44 31.44C287.4 401.9 273.4 416 256 416z"/></svg>  
    <strong>Warning:</strong> The refrigerator must be completely level and will not operate if not parked on a <b>flat surface</b>.
</div>


<a href="pre-departure.html"><button class="nav-button"><i class="arrow arrow-left"></i> Pre-Departure</button></a>
<a href="pre-return.html" class="right"><button class="nav-button">Pre-Return <i class="arrow arrow-right"></i></button></a>

{% include google-analytics.html %}