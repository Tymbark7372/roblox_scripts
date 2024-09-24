-- MADE BY Tymbark7372

-- 7 is W, 8 is S. to spam click 3

-- you can change the wait by adding bigger number

local UserInputService = game:GetService("UserInputService")
local isSpamming = false
local spamConnection

local function spamSW()
    local virtualInput = game:GetService("VirtualInputManager")
    while isSpamming do
        virtualInput:SendKeyEvent(true, Enum.KeyCode.S, false, game)
        wait(0.1)
        virtualInput:SendKeyEvent(false, Enum.KeyCode.S, false, game)
        wait(0.1)
        virtualInput:SendKeyEvent(true, Enum.KeyCode.W, false, game)
        wait(0.1)
        virtualInput:SendKeyEvent(false, Enum.KeyCode.W, false, game)
        wait(0.1)
    end
end

UserInputService.InputBegan:Connect(function(input)
    local virtualInput = game:GetService("VirtualInputManager")

    if input.KeyCode == Enum.KeyCode.Three then
        isSpamming = not isSpamming
        if isSpamming then
            spamConnection = coroutine.wrap(spamSW) 
            spamConnection()
        end
    elseif input.KeyCode == Enum.KeyCode.Seven then
        virtualInput:SendKeyEvent(true, Enum.KeyCode.W, false, game)
        wait(0.1)
        virtualInput:SendKeyEvent(false, Enum.KeyCode.W, false, game)
    elseif input.KeyCode == Enum.KeyCode.Eight then
        virtualInput:SendKeyEvent(true, Enum.KeyCode.S, false, game)
        wait(0.1)
        virtualInput:SendKeyEvent(false, Enum.KeyCode.S, false, game)
    end
end)
