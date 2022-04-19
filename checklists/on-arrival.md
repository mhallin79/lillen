<link href="../styles/custom.css" rel="stylesheet" />
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script type="text/javascript">
    $(function(){
        var toggleTypes = ['powerToggle', 'waterToggle', 'greywaterToggle'];
        $.each(toggleTypes, function(i, toggleType){
            var checkboxTarget = $('input[name="' + toggleType + '"]').data('target');
            $('input[name="' + toggleType + '"]').on('change', function(e){
                var label = $('label input[name="' + toggleType + '"]').each(function(i, el){
                    $(el).parent().removeClass('checked');
                }).parent();

                var checkedRadio = $('input[name="' + toggleType + '"]:checked');
                checkedRadio.parent().addClass('checked');

                $('label.'+ checkboxTarget).css('display', (checkedRadio.val() == 'Y' ? 'block' : 'none'));
            });
            $('input[name="' + toggleType + '"]:checked').parent().addClass('checked');
            $('label.'+checkboxTarget).css({ display: 'none'}); // initial hide            
        });
    });
</script>

# On Arrival

<ol class="yesnolist">
    <li>
        <p>Does the site have power to connect?</p>
        <label title="yes"><input type="radio" name="powerToggle" class="radioToggle" value="Y" data-target="power" /> Yes</label>
        <label title="no"><input type="radio" name="powerToggle" class="radioToggle" value="N" data-target="power" checked="checked" /> No</label>
    </li>
    <li>
        <p>Does the site have water to connect?</p>
        <label title="yes"><input type="radio" name="waterToggle" class="radioToggle" value="Y" data-target="water" /> Yes</label>
        <label title="no"><input type="radio" name="waterToggle" class="radioToggle" value="N" data-target="water" checked="checked" /> No</label>
    </li>
    <li>
        <p>Does the site have greywater to connect?</p>
        <label title="yes"><input type="radio" name="greywaterToggle" class="radioToggle" value="Y" data-target="greywater" /> Yes</label>
        <label title="no"><input type="radio" name="greywaterToggle" class="radioToggle" value="N" data-target="greywater" checked="checked" /> No</label>
    </li>
</ol>

## Checklist

<label for="parking"><input type="checkbox" id="parking"/> Select as flat and level a parking site as possible. Use leveling blocks if
required.</label>
<label for="power" class="power"><input type="checkbox" id="power" /> Connect 240v electricity <br />
*Check if [15A to 10A Power Adaptor](../guides/power-adaptor.md) is required.*</label>
<label for="city-water" class="water"><input type="checkbox" id="city-water" /> Connect city water </label>
<label for="grey-water" class="greywater"><input type="checkbox" id="grey-water" /> Connect grey water </label>
<label for="lpg"><input type="checkbox" id="lpg"/> Ensure LPG gas bottle is open</label>
<label for="control-panel"><input type="checkbox" id="control-panel"/> Turn on button 1-3 on the [Battery and Water Control Panel](../guides/control-panel.md).</label>
<label for="water-pump"><input type="checkbox" id="water-pump"/> Turn the water pump on, if not connected to city water.<br/>
*Button 4 on the [Battery and Water Control Panel](../guides/control-panel.md)*
</label>
<label for="water-heater"><input type="checkbox" id="water-heater"/> Turn the hot water heater on using either 240v or LPG gas.</label>
<label for="refrigerator"><input type="checkbox" id="refrigerator"/> Ensure the refrigerator (in auto mode) switch to either 240v or LPG gas.</label>
<label for="lpg-level"><input type="checkbox" id="lpg-level"/> If using LPG gas, turn the refrigerator fan on.</label>

> **Please note!** If using LPG gas, it can take up to **20 minutes** before the fridge turns on. 
>
> The refrigerator must be level and will not operate if not parked on a flat surface.


<a href="pre-departure.html"><button class="nav-button"><i class="arrow arrow-left"></i> Pre-Departure</button></a>
<a href="pre-return.html" class="right"><button class="nav-button">Pre-Return <i class="arrow arrow-right"></i></button></a>