local bit = {}

function bit.lshift(x, n)
    return x * (2 ^ n)
end

function bit.rshift(x, n)
    return math.floor(x / (2 ^ n))
end

function bit.band(x, y)
    local result = 0
    local bitval = 1
    while x > 0 and y > 0 do
        if x % 2 == 1 and y % 2 == 1 then
            result = result + bitval
        end
        bitval = bitval * 2
        x = math.floor(x / 2)
        y = math.floor(y / 2)
    end
    return result
end

function bit.bor(x, y)
    local result = 0
    local bitval = 1
    while x > 0 or y > 0 do
        if x % 2 == 1 or y % 2 == 1 then
            result = result + bitval
        end
        bitval = bitval * 2
        x = math.floor(x / 2)
        y = math.floor(y / 2)
    end
    return result
end

function bit.bxor(x, y)
    local result = 0
    local bitval = 1
    while x > 0 or y > 0 do
        if (x % 2 == 1 and y % 2 == 0) or (x % 2 == 0 and y % 2 == 1) then
            result = result + bitval
        end
        bitval = bitval * 2
        x = math.floor(x / 2)
        y = math.floor(y / 2)
    end
    return result
end

function bit.bnot(n)
    local p = 2^32
    return p - 1 - n
end
return bit
