# Anti-Xray

Anti Xray é um mod Fabric leve que permite aos proprietários de servidores combater os xrayers.

## Configurações

```toml
# Valores padrão
enabled = false

# Valores especificos de mundo
[overworld]
enabled = true
engineMode = 3
maxBlockHeight = 256
updateRadius = 2
lavaObscures = false
hiddenBlocks = ["#c:ores", "raw_copper_block", "raw_iron_block", "raw_gold_block"]
replacementBlocks = ["stone", "deepslate", "andesite", "calcite", "diorite", "dirt", "granite", "gravel", "sand", "tuff", "mossy_cobblestone", "obsidian", "clay", "infested_stone", "amethyst_block", "budding_amethyst", "chest"]

[the_nether]
enabled = true
engineMode = 1
maxBlockHeight = 128
updateRadius = 2
lavaObscures = true
hiddenBlocks = ["ancient_debris", "nether_quartz_ore", "nether_gold_ore", "gold_block", "gilded_blackstone"]
```

### Visão geral das opções de configuração

`enabled` se definido como verdadeiro, o anti xray estará ativo no mundo especificado

`engineMode` pode ser 1, 2 ou 3, cnfira [Engine Modes](#Engine Modes)

`maxBlockHeight` controla a altura máxima na qual os blocos devem ficar ofuscados

`updateRadius` controla a quantos blocos de distância dos blocos mostrados a ofuscação deve começar (se seus jogadores virem minérios falsos
recomenda-se aumentar este valor)

`lavaObscures` se definido como verdadeiro, os blocos próximos à lava ficarão obscurecidos

`hiddenBlocks` lista de blocos para esconder *(Engine mode 1)* ou uma lista de blocos para usar para ofuscação *(Engine mode 2/3)*

`replacementBlocks` é uma lista de blocos que serão ofuscados, mas não considerados blocos falsos *(apenas Engine mode 2/3)*

**Visão legit do jogador:** Jogadores legits não notarão nenhuma mudança quando este mod for instalado (a menos que tenham ping alto ou modifiquem muitos blocos de uma vez, por exemplo: explosões)

### Dimensões Customizadas
Para configurar o antixray em dimensões personalizadas, especifique o ID da dimensão assim: `["custom:cool_world"]`
