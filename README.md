local player = game:GetService("Players").LocalPlayer
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UIStroke = Instance.new("UIStroke") -- Borda Roxa
local WelcomeText = Instance.new("TextLabel")
local VersionText = Instance.new("TextLabel")
local PortugueseButton = Instance.new("TextButton")
local EnglishButton = Instance.new("TextButton")
local SelectionText = Instance.new("TextLabel") -- Mensagem de seleção

-- Configuração da ScreenGui
ScreenGui.Parent = player:WaitForChild("PlayerGui")

-- Configuração do Frame (Interface mais larga e menor na altura)
Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0) -- Fundo Preto
Frame.Size = UDim2.new(0, 500, 0, 180) -- Largura maior e altura menor
Frame.Position = UDim2.new(0.5, -250, 0.5, -90)

-- borda roxa Ai papai
UIStroke.Parent = Frame
UIStroke.Thickness = 4
UIStroke.Color = Color3.fromRGB(150, 0, 255) -- Roxo

-- Configuração do Texto de Boas-Vindas
WelcomeText.Parent = Frame
WelcomeText.Text = "Bem vindo ao Bazuka Hub!"
WelcomeText.Size = UDim2.new(1, 0, 1, 0)
WelcomeText.TextColor3 = Color3.fromRGB(255, 255, 255) -- Letras Brancas
WelcomeText.BackgroundTransparency = 1
WelcomeText.Font = Enum.Font.GothamBlack
WelcomeText.TextScaled = true

-- Aguarda 2 segundos e some com a mensagem
task.wait(2)
WelcomeText:Destroy()

-- Configuração do Texto de Escolha de Versão
VersionText.Parent = Frame
VersionText.Text = "Qual versão deseja usar?"
VersionText.Size = UDim2.new(1, 0, 0.3, 0)
VersionText.Position = UDim2.new(0, 0, 0.1, 0)
VersionText.TextColor3 = Color3.fromRGB(255, 255, 255) -- Letras Brancas
VersionText.BackgroundTransparency = 1
VersionText.Font = Enum.Font.GothamBlack
VersionText.TextScaled = true

-- Configuração do Botão Português 🇧🇷
PortugueseButton.Parent = Frame
PortugueseButton.Text = "🇧🇷 Português"
PortugueseButton.Size = UDim2.new(0.45, 0, 0.3, 0)
PortugueseButton.Position = UDim2.new(0.05, 0, 0.6, 0)
PortugueseButton.BackgroundColor3 = Color3.fromRGB(0, 150, 0)
PortugueseButton.TextColor3 = Color3.fromRGB(255, 255, 255)
PortugueseButton.Font = Enum.Font.GothamBold
PortugueseButton.TextScaled = true
PortugueseButton.BorderSizePixel = 2

-- Configuração do BotãoPortuguês 2 🇧🇷
EnglishButton.Parent = Frame
EnglishButton.Text = "🇧🇷 Português 2"
EnglishButton.Size = UDim2.new(0.45, 0, 0.3, 0)
EnglishButton.Position = UDim2.new(0.5, 0, 0.6, 0)
EnglishButton.BackgroundColor3 = Color3.fromRGB(0, 0, 200)
EnglishButton.TextColor3 = Color3.fromRGB(255, 255, 255)
EnglishButton.Font = Enum.Font.GothamBold
EnglishButton.TextScaled = true
EnglishButton.BorderSizePixel = 2

-- Configuração do Texto de Seleção
SelectionText.Parent = Frame
SelectionText.Size = UDim2.new(1, 0, 1, 0)
SelectionText.TextColor3 = Color3.fromRGB(255, 255, 255)
SelectionText.BackgroundTransparency = 1
SelectionText.Font = Enum.Font.GothamBlack
SelectionText.TextScaled = true
SelectionText.Visible = false -- Inicialmente escondido

-- remover a interface e carregar o script em Português XD
PortugueseButton.MouseButton1Click:Connect(function()
VersionText.Visible = false
PortugueseButton.Visible = false
EnglishButton.Visible = false

-- Exibe a mensagem de seleção por 1,5 segundos
SelectionText.Text = "Selecionado: ESP PRINCIPAL"
SelectionText.Visible = true
task.wait(1.5)

ScreenGui:Destroy()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Bazukalindao/esp/refs/heads/main/README.md"))()

end)

-- remover a interface e carregar o script em Inglês XD
EnglishButton.MouseButton1Click:Connect(function()
VersionText.Visible = false
PortugueseButton.Visible = false
EnglishButton.Visible = false

SelectionText.Text = "selecionado: ESP BASICO"
SelectionText.Visible = true
task.wait(1.5)

ScreenGui:Destroy()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Bazukalindao/espRGB/refs/heads/main/README.md"))()

end)
