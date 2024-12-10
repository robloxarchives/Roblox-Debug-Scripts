-- For context, get kicked by your anti-cheat before running this script
local a=game:GetService("GuiService")
local b={}
local c=0

local function d(e)
    for f,g in pairs(game:GetDescendants())do 
        if g:IsA("TextLabel") and g.Text:find(e) then 
            print("Deleting: "..g:GetFullName())  -- Print the full path of the object
            g:Destroy()
        end 
    end 
end

while task.wait(0.5)do 
    local h=a:GetErrorMessage()
    if h~=""then 
        print("Error detected: "..h)
        b[h]=(b[h]or 0)+1
        a:ClearError()
        d(h)
    end
    c=c+0.5
    if c>=60 then 
        for e,i in pairs(b)do 
            print("Error: '"..e.."' occurred "..i.." times.")
        end
        c=0 
    end 
end
