<script lang="ts">
    import type { PageData } from './$types';
    
    export let data: PageData;

    import Card, {
      Content,
      Actions
    } from '@smui/card';
    import Button, { Label } from '@smui/button';
    import Textfield from '@smui/textfield';
    import Icon from '@smui/textfield/icon';
    import HelperText from '@smui/textfield/helper-text';

    let firefly_iii_url = '';
    let firefly_iii_api_key = '';
</script>

<style>
  .card-container {
    margin: auto;
    width: 390px;
  }
</style>

<div class="card-container">
  <Card>
    <Content>
      <h3 style="margin-top: 10px; margin-bottom: 10px;">Login</h3>
      <div>
        <Textfield bind:value={firefly_iii_url} label="Firefly III URL" style="width: 100%;">
          <Icon class="material-icons" slot="leadingIcon">http</Icon>
          <HelperText slot="helper">URL to Firefly III</HelperText>
        </Textfield>
      </div>
      <div>
        <Textfield bind:value={firefly_iii_api_key} label="Firefly III API key" style="width: 100%;">
          <Icon class="material-icons" slot="leadingIcon">key</Icon>
          <HelperText slot="helper">Firefly III API key</HelperText>
        </Textfield>
      </div>
    </Content>
    <Actions>
      <Button on:click={() => null}>
        <Label>Login</Label>
        <i class="material-icons" aria-hidden="true">arrow_forward</i>
      </Button>
    </Actions>
  </Card>
</div>