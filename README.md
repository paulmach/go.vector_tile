go.vector_tile
==============

Package vector_tile provides the Go (Golang) code needed to read and write
[Mapbox vector tiles](https://github.com/mapbox/vector-tile-spec).
Most of the code is the auto generated [protobuf](https://developers.google.com/protocol-buffers/docs/overview)
language bindings, but there are a few helpers
to make encoding and decoding the tiles a little easier.

[![Godoc Reference](https://godoc.org/github.com/paulmach/go.vector_tile?status.png)](https://godoc.org/github.com/paulmach/go.vector_tile)

## Helper Functions

	// Encode protobuf encodes the tile into a byte buffer.
	func Encode(tile *Tile) ([]byte, error)

	// EncodeGzipped gzips the data after encoding the tile via protocol buffers.
	func EncodeGzipped(tile *Tile) ([]byte, error)

	// Decode has the protobuf library decode the data into a tile.
	func Decode(data []byte) (*Tile, error)

	// DecodeGzipped first ungzips the data before having the
	// protobuf library decode the data into a tile.
	func DecodeGzipped(data []byte) (*Tile, error)
