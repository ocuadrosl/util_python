def image_to_tiles(image, tile_size):
    """
        Split image into tiles of size tileSize
        Notice tiles are non-overlapping patches
        if the sizes do not match, the last small patch is ignored
    """

    height, width, _ = image.shape
    # print(image.shape)

    tiles = []
    positions = []

    # max possible sizes
    max_height = height - (height % tile_size)
    max_width = width - (width % tile_size)

    # print(max_height, max_width)
    for i in range(0, max_height, tile_size):
        for j in range(0, max_width, tile_size):

            positions.append(np.asarray((i, i + tile_size, j, j + tile_size)))
            tiles.append(image[i:i + tile_size, j:j + tile_size])

    # print(image[i:i+tileSize, j:j+tileSize])
    # lastTile = image[max_height:height, max_width:width]
    # if lastTile.shape[0] > 0 and lastTile.shape[1] > 0:
    #    tiles.append(lastTile)
    #    positions.append(np.asarray((max_height, height, max_width, width)))
    return tiles, positions
