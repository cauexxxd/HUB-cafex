-- Hub Exclusivo: Cafex
-- Certifique-se de usar este script de forma responsável!

local CafexKey = "cafex" -- Chave exclusiva do Hub

-- Verificar chave
local function verifyKey(inputKey)
    if inputKey == CafexKey then
        print("Bem-vindo ao Hub Cafex!")
        return true
    else
        print("Chave incorreta. Acesso negado.")
        return false
    end
end

-- Menu principal
local function showMenu()
    print("=== Menu Cafex ===")
    print("1. Farm de Nível")
    print("2. Teletransporte")
    print("Digite o número da opção desejada:")
end

-- Função de farm de nível
local function farmLevel()
    print("Farm de nível iniciado...")
    -- Insira sua lógica personalizada de farm aqui
end

-- Função de teletransporte
local function teleportToLocation(location)
    print("Teletransportando para: " .. location)
    -- Insira a lógica de teletransporte aqui
end

-- Execução do script
print("Por favor, insira a chave do Hub Cafex:")
local userInput = io.read()

if verifyKey(userInput) then
    showMenu()
    local choice = io.read()

    if choice == "1" then
        farmLevel()
    elseif choice == "2" then
        print("Digite o local para teletransporte:")
        local location = io.read()
        teleportToLocation(location)
    else
        print("Opção inválida!")
    end
end

