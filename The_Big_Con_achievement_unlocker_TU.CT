<?xml version="1.0" encoding="utf-8"?>
<CheatTable CheatEngineTableVersion="45">
  <CheatEntries>
    <CheatEntry>
      <ID>5</ID>
      <Description>"Enable Achievement Unlocker"</Description>
      <Options moHideChildren="1" moDeactivateChildrenAsWell="1"/>
      <LastState/>
      <Color>008000</Color>
      <VariableType>Auto Assembler Script</VariableType>
      <AssemblerScript>{ Game   : The Big Con.exe
  Version: 1.4.17.0 | Windows Store
  Date   : 2024-03-12
  Author : SvT + (title update by Ethan)
}

[ENABLE]
LuaCall(function cycleFullCompact(sender,force) local state = not(compactmenuitem.Caption == 'Compact View Mode'); if force~=nil then state = not force end; compactmenuitem.Caption = state and 'Compact View Mode' or 'Full View Mode'; getMainForm().Splitter1.Visible = state; getMainForm().Panel4.Visible    = state; getMainForm().Panel5.Visible    = state; end; function addCompactMenu() if compactmenualreadyexists then return end; local parent = getMainForm().Menu.Items; compactmenuitem = createMenuItem(parent); parent.add(compactmenuitem); compactmenuitem.Caption = 'Compact View Mode'; compactmenuitem.OnClick = cycleFullCompact; compactmenualreadyexists = 'yes'; end; addCompactMenu(); cycleFullCompact(nil,true))

{$lua}
LaunchMonoDataCollector()

  if (syntaxcheck) then return end
  local cls = GetLuaEngine()
           cls.mOutput.Lines.Clear()

     local domain = mono_enumDomains()[1]
     local klass = mono_findClass('', 'PlatformHelper')
     local instance = mono_class_findInstancesOfClassListOnly(domain,klass)

        for k,v in pairs(instance) do

        local BaseAddress = getAddressSafe(v)

        local InitializationStatus_offset = 0x30
        local InitializationStatus_address = getAddress(BaseAddress + InitializationStatus_offset)
        local InitializationStatus_value = readInteger(InitializationStatus_address)

        local addressList = getAddressList()
        local debugBox = addressList.getMemoryRecordByDescription('DEBUG (enable this first)')

        if (InitializationStatus_value == 2) then
           registerSymbol("instanceAddress",instance[k])
           if debugBox.Active == true then
              output1 = '[ %s ] --&gt; Instance ( %X ) --&gt; InitializationStatus_address [ %X ] --&gt; InitializationStatus_value hex: ( %08X ) &lt;-- int: ( %s )'
              print((output1):format(k,instance[k],InitializationStatus_address,InitializationStatus_value or 0,InitializationStatus_value))
              print("TRUE : conditions met \n")
           end
        else
            if debugBox.Active == true then
               print("FALSE : conditions not met \n")
            end
        end
     end

{$asm}

[DISABLE]
LuaCall(cycleFullCompact(nil,false))

unregistersymbol(instanceAddress)
</AssemblerScript>
      <CheatEntries>
        <CheatEntry>
          <ID>126</ID>
          <Description>"instanceAddress"</Description>
          <LastState Value="" RealAddress="1CD6A764840"/>
          <ShowAsHex>1</ShowAsHex>
          <ShowAsSigned>0</ShowAsSigned>
          <Color>0000FA</Color>
          <VariableType>Array of byte</VariableType>
          <ByteLength>0</ByteLength>
          <Address>instanceAddress</Address>
        </CheatEntry>
        <CheatEntry>
          <ID>127</ID>
          <Description>"Achievements"</Description>
          <LastState Value="" RealAddress="00000000"/>
          <Color>008000</Color>
          <GroupHeader>1</GroupHeader>
          <CheatEntries>
            <CheatEntry>
              <ID>145</ID>
              <Description>"Lorgo and the Flungus"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "10"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>179</ID>
              <Description>"That's a Good Flungus"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "11"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>140</ID>
              <Description>"The Bandcamp Baint 'n Switch"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "1"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>162</ID>
              <Description>"The Best Friend Shuffle"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "28"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>147</ID>
              <Description>"The Big Con"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "8"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>156</ID>
              <Description>"The Big Cornucopia"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "34"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>172</ID>
              <Description>"The Big Sneak"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "18"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>144</ID>
              <Description>"The Burblo Boondoggle"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "2"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>148</ID>
              <Description>"The Casino Case-Out"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "7"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>152</ID>
              <Description>"The Collector's Gambit"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "38"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>141</ID>
              <Description>"The Desert Dialtone"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "5"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>165</ID>
              <Description>"The Dusty Toss"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "25"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>153</ID>
              <Description>"The Film Buff"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "37"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>161</ID>
              <Description>"The First Timer"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "29"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>146</ID>
              <Description>"The Flin Flon Flimflam"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "9"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>158</ID>
              <Description>"The Fraudster"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "32"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>166</ID>
              <Description>"The Heatstroke Hallucination"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "24"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>143</ID>
              <Description>"The Hormliner Hustle"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "3"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>164</ID>
              <Description>"The Huxtor's Finest"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "26"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>177</ID>
              <Description>"The Joker"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "13"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>142</ID>
              <Description>"The Kabaczky Confusion"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "4"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>170</ID>
              <Description>"The Last Minute Birthday Party"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "20"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>167</ID>
              <Description>"The Legitimate Hustle"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "23"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>175</ID>
              <Description>"The Lover"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "15"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>171</ID>
              <Description>"The Old Switcheroo"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "19"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>174</ID>
              <Description>"The Periwinkle Takeover"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "16"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>159</ID>
              <Description>"The Protectionist"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "31"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>176</ID>
              <Description>"The Smoker"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "14"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>173</ID>
              <Description>"The Squeaky Stranger"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "17"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>149</ID>
              <Description>"The Suit-Up Surprise"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "6"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>163</ID>
              <Description>"The Tape Never Lies"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "27"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>169</ID>
              <Description>"The Truth"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "21"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>157</ID>
              <Description>"The Watcher"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "33"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>168</ID>
              <Description>"The Whole Truth"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "22"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>178</ID>
              <Description>"Third Time's a Flungus"</Description>
              <LastState/>
              <VariableType>Auto Assembler Script</VariableType>
              <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "12"}})
{$asm}
[DISABLE]
</AssemblerScript>
            </CheatEntry>
            <CheatEntry>
              <ID>180</ID>
              <Description>"Grift of the Year Edition (free Title Update)"</Description>
              <LastState Value="" RealAddress="00000000"/>
              <Color>808000</Color>
              <GroupHeader>1</GroupHeader>
              <CheatEntries>
                <CheatEntry>
                  <ID>183</ID>
                  <Description>"Sticky Fingers Casino"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "48"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>186</ID>
                  <Description>"Sticky Fingers Las Venganza"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "45"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>184</ID>
                  <Description>"Sticky Fingers Las Venganza Revisted"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "47"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>189</ID>
                  <Description>"Sticky Fingers Lisbon"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "42"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>188</ID>
                  <Description>"Sticky Fingers Mallton"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "43"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>187</ID>
                  <Description>"Sticky Fingers Midlands Hormliner"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "44"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>185</ID>
                  <Description>"Sticky Fingers Perdido"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "46"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>192</ID>
                  <Description>"The Changebreaker"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "50"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>191</ID>
                  <Description>"The Giant Block of Horm"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "51"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>151</ID>
                  <Description>"The Skater"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "39"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>190</ID>
                  <Description>"The Stickiest Situation"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "41"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>150</ID>
                  <Description>"The Three Kids In A Trench Coat"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "40"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>182</ID>
                  <Description>"The Video Store Employee"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "30"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>182</ID>
                  <Description>"The Taking Candy from a Baby"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "52"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>182</ID>
                  <Description>"A Rad Achievement"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "53"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>182</ID>
                  <Description>"A Radder Achievement"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "54"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
                <CheatEntry>
                  <ID>182</ID>
                  <Description>"THE RADDEST ACHIEVEMENT"</Description>
                  <LastState/>
                  <VariableType>Auto Assembler Script</VariableType>
                  <AssemblerScript>[ENABLE]
{$lua}
if (syntaxcheck) then return end
mono_invoke_method(nil, mono_findMethod('','PlatformHelper', 'UnlockAchievement'), getAddress('instanceAddress'), {{type = vtString, value = "49"}})
{$asm}
[DISABLE]
</AssemblerScript>
                </CheatEntry>
              </CheatEntries>
            </CheatEntry>
          </CheatEntries>
        </CheatEntry>
      </CheatEntries>
    </CheatEntry>
    <CheatEntry>
      <ID>38</ID>
      <Description>"DEBUG (enable this first)"</Description>
      <Options moHideChildren="1"/>
      <LastState Value="" RealAddress="00000000"/>
      <Color>0000FA</Color>
      <GroupHeader>1</GroupHeader>
      <CheatEntries>
        <CheatEntry>
          <ID>33</ID>
          <Description>"instanceAddress"</Description>
          <LastState Value="" RealAddress="1CD6A764840"/>
          <ShowAsSigned>0</ShowAsSigned>
          <Color>0000FA</Color>
          <VariableType>Array of byte</VariableType>
          <ByteLength>0</ByteLength>
          <Address>instanceAddress</Address>
          <CheatEntries>
            <CheatEntry>
              <ID>128</ID>
              <Description>"InitializationStatus"</Description>
              <LastState Value="2" RealAddress="1CD6A764870"/>
              <ShowAsSigned>0</ShowAsSigned>
              <VariableType>Byte</VariableType>
              <Address>+30</Address>
            </CheatEntry>
          </CheatEntries>
        </CheatEntry>
      </CheatEntries>
    </CheatEntry>
  </CheatEntries>
  <UserdefinedSymbols/>
</CheatTable>
